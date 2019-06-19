---
title: AX 2012 からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations へのデータ アップグレードに関連付けられている Microsoft DynamicsAX 2012 チェックリストの各タスクについて説明します。
author: robadawy
manager: AnnBe
ms.date: 02/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 5643f86ecc842629bda864cfe91efe11dc0803f4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560631"
---
# <a name="upgrade-from-ax-2012---pre-upgrade-checklist-for-data-upgrade"></a><span data-ttu-id="a137a-103">AX 2012 からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト</span><span class="sxs-lookup"><span data-stu-id="a137a-103">Upgrade from AX 2012 - Pre-upgrade checklist for data upgrade</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="a137a-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations へのデータ アップグレードに関連付けられている Microsoft DynamicsAX 2012 チェックリストの各タスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a137a-104">This topic describes each task in the Microsoft Dynamics AX 2012 checklist that is associated with data upgrade to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="installation"></a><span data-ttu-id="a137a-105">インストール</span><span class="sxs-lookup"><span data-stu-id="a137a-105">Installation</span></span>
<span data-ttu-id="a137a-106">アップグレード前のチェックリストを使用して、アップグレード手順に必要なデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="a137a-106">Use the pre-upgrade checklist to enter data that will be required for the upgrade procedure.</span></span> 

- <span data-ttu-id="a137a-107">AX 2012 R3 からアップグレードする場合は、[KB 4035163](https://go.microsoft.com/fwlink/?linkid=852255) をインストールします</span><span class="sxs-lookup"><span data-stu-id="a137a-107">If upgrading from AX 2012 R3, install [KB 4035163](https://go.microsoft.com/fwlink/?linkid=852255)</span></span>
- <span data-ttu-id="a137a-108">AX 2012 R2 からアップグレードする場合は、[KB 4048614](https://go.microsoft.com/fwlink/?linkid=869025) をインストールします</span><span class="sxs-lookup"><span data-stu-id="a137a-108">if upgrading from AX 2012 R2, install [KB 4048614](https://go.microsoft.com/fwlink/?linkid=869025)</span></span>

## <a name="prepare-model-metadata"></a><span data-ttu-id="a137a-109">モデル メタデータの準備</span><span class="sxs-lookup"><span data-stu-id="a137a-109">Prepare model metadata</span></span>

<span data-ttu-id="a137a-110">データ アップグレード中に、既存の AX 2012 環境とアップグレードされた Finance and Operations との間で要素 IDs を維持することが 1 つの目標です。</span><span class="sxs-lookup"><span data-stu-id="a137a-110">During data upgrade, one goal is to maintain element IDs between the existing AX 2012 environment and the upgraded Finance and Operations environment.</span></span> <span data-ttu-id="a137a-111">この目標を達成するには、AX 2012 環境の要素 ID のコピーを Finance and Operations 環境に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a137a-111">To accomplish this goal, you must bring a copy of the element IDs from the AX 2012 environment into the Finance and Operations environment.</span></span> <span data-ttu-id="a137a-112">AX 2012 は、ModelElement という名前のテーブルに要素の ID を格納します。</span><span class="sxs-lookup"><span data-stu-id="a137a-112">AX 2012 stores element IDs in a table that is named ModelElement.</span></span> <span data-ttu-id="a137a-113">このテーブルは、AX 2012 ビジネス データ データベースとは別のデータベースであるモデル データベースに含まれています。</span><span class="sxs-lookup"><span data-stu-id="a137a-113">This table is in the model database, which is a separate database from the AX 2012 business data database.</span></span> <span data-ttu-id="a137a-114">Finance and Operations にアップグレード中に、Microsoft Azure に AX 2012 データベースをコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a137a-114">During an upgrade to Finance and Operations, you must copy the AX 2012 database to Microsoft Azure.</span></span> <span data-ttu-id="a137a-115">このプロセスには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a137a-115">This process can be time consuming.</span></span> 

<span data-ttu-id="a137a-116">model データベース全体を Azure SQL データベースにコピーしないようにするには、次の手順を使用して ModelElement テーブルをビジネス データ データベースに複製します。</span><span class="sxs-lookup"><span data-stu-id="a137a-116">To avoid copying the whole model database to Azure SQL Database, use the following procedure to replicate the ModelElement table in the business data database.</span></span> <span data-ttu-id="a137a-117">後ほど、データのアップグレード実行中に、データベースの同期プロセスがこのレプリケートされたテーブルから必要な情報を取得し、アップグレードされた Finance and Operations 環境で要素 ID が管理されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a137a-117">Later, during data upgrade runs, the database synchronization process will retrieve the required information from this replicated table and make sure that element IDs are maintained in the upgraded Finance and Operations environment.</span></span>

1. <span data-ttu-id="a137a-118">Finance and Operations のデータ アップグレード チェックリストで、**モデル メタデータの準備**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a137a-118">In the Finance and Operations data upgrade checklist, click **Prepare model metadata**.</span></span>
2. <span data-ttu-id="a137a-119">メッセージが表示されたら、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a137a-119">When you’re prompted, click **Yes**.</span></span>
3. <span data-ttu-id="a137a-120">コピー処理が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="a137a-120">Wait for the copy process to be completed.</span></span>

<span data-ttu-id="a137a-121">プロセスが正常に行われた場合は、タスクは完了としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="a137a-121">If the process is successful, the task is marked as completed.</span></span>

## <a name="prepare-security-role-metadata"></a><span data-ttu-id="a137a-122">セキュリティ ロール メタデータの準備</span><span class="sxs-lookup"><span data-stu-id="a137a-122">Prepare security role metadata</span></span>

<span data-ttu-id="a137a-123">データ アップグレード中のもう 1 つの目標は、セキュリティ ロールの割り当てを維持することです。</span><span class="sxs-lookup"><span data-stu-id="a137a-123">Another goal during data upgrade is to preserve security role assignments.</span></span> <span data-ttu-id="a137a-124">このタスクは、前の「モデル メタデータの準備」タスクに似ています。</span><span class="sxs-lookup"><span data-stu-id="a137a-124">This task resembles the previous “Prepare model metadata” task.</span></span> <span data-ttu-id="a137a-125">AX 2012 モデル データベースに格納されているセキュリティ ロールの情報は、アップグレード後も情報が Finance and Operations 環境に残るように、AX 2012 ビジネス データ データベースにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a137a-125">Security role information that is stored in the AX 2012 model database must be copied to the AX 2012 business data database, so that the information is preserved in the Finance and Operations environment after upgrade.</span></span> <span data-ttu-id="a137a-126">データ アップグレード中に、同じセキュリティ ロールは更新された Finance and Operations の環境に戻されます。</span><span class="sxs-lookup"><span data-stu-id="a137a-126">During data upgrade runs, the same security role will be restored in the upgraded Finance and Operations environment.</span></span>

1. <span data-ttu-id="a137a-127">Dynamics 365 for Finance and Operations データ アップグレードのチェックリストで、**セキュリティ ロール メタデータを準備する**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a137a-127">In the Dynamics 365 for Finance and Operations data upgrade checklist, click **Prepare security role metadata**.</span></span>
1. <span data-ttu-id="a137a-128">メッセージが表示されたら、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a137a-128">When you’re prompted, click **Yes**.</span></span>
1. <span data-ttu-id="a137a-129">コピー処理が完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="a137a-129">Wait for the copy process to be completed.</span></span>

<span data-ttu-id="a137a-130">プロセスが正常に行われた場合は、タスクは完了としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="a137a-130">If the process is successful, the task is marked as completed.</span></span>

## <a name="set-up-user-mapping"></a><span data-ttu-id="a137a-131">ユーザー マッピングの設定</span><span class="sxs-lookup"><span data-stu-id="a137a-131">Set up user mapping</span></span>

<span data-ttu-id="a137a-132">AX 2012 では、ユーザーはオンプレミスの Active Directory サーバーで認証されます。</span><span class="sxs-lookup"><span data-stu-id="a137a-132">In AX 2012, users are authenticated against an on-premises Active Directory server.</span></span> <span data-ttu-id="a137a-133">ただし、Finance and Operations では、ユーザーは、Azure Active Directory (Azure AD) に対して認証されます。</span><span class="sxs-lookup"><span data-stu-id="a137a-133">However, in Finance and Operations, users are authenticated against Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="a137a-134">このタスクは、既存の AX 2012 ユーザーを同等 Azure AD にマップするフォームを提供します。</span><span class="sxs-lookup"><span data-stu-id="a137a-134">This task provides a form where you can map existing AX 2012 users to equivalent Azure AD users.</span></span> <span data-ttu-id="a137a-135">AX 2012 ユーザーは、Finance and Operations にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="a137a-135">The AX 2012 users will then be able to access Finance and Operations.</span></span>

1. <span data-ttu-id="a137a-136">Finance and Operations のデータ アップグレード チェックリストで、**ユーザー マッピングの設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a137a-136">In the Finance and Operations data upgrade checklist, click **Set up user mapping**.</span></span>
2. <span data-ttu-id="a137a-137">**ユーザー情報電子メール マッピング** フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a137a-137">The **User info email mapping** form appears.</span></span> <span data-ttu-id="a137a-138">グリッドに記入するには、次のいずれかのステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="a137a-138">Follow one of these steps to fill in the grid:</span></span>
   - <span data-ttu-id="a137a-139">AX 2012 からユーザーをインポートしてから、手動で Azure AD の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a137a-139">Import users from AX 2012, and then manually fill in the Azure AD email address:</span></span>
       1. <span data-ttu-id="a137a-140">**AX からインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a137a-140">Click **Import from AX**.</span></span> <span data-ttu-id="a137a-141">グリッドには既存のユーザーが入力されます</span><span class="sxs-lookup"><span data-stu-id="a137a-141">The grid is filled with existing users.</span></span>
       1. <span data-ttu-id="a137a-142">各ユーザーについては、次の図に示すように、対応する Azure AD 電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="a137a-142">For each user, enter the corresponding Azure AD email address, as shown in the following illustration.</span></span>

           ![AX 2012 ユーザーの Azure AD 電子メール アドレス](media/userInfoEmailMapping.png)

   - <span data-ttu-id="a137a-144">ファイルからユーザーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="a137a-144">Import users from a file.</span></span> <span data-ttu-id="a137a-145">このオプションは高速です。</span><span class="sxs-lookup"><span data-stu-id="a137a-145">This option is faster.</span></span> <span data-ttu-id="a137a-146">多くのユーザーを更新する必要があるときは、このオプションを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a137a-146">We recommend that you use this option when many users must be updated.</span></span>

     1. <span data-ttu-id="a137a-147">コンマ区切り値 (CSV) ファイルで、AX 2012 ユーザーと Azure AD 電子メール アドレスのマッピングを作成します。</span><span class="sxs-lookup"><span data-stu-id="a137a-147">In a comma-separated values (CSV) file, create the mapping between AX 2012 users and Azure AD email addresses.</span></span> <span data-ttu-id="a137a-148">IT 部門は、オンプレミスの Active Directory ドメイン サービスから同様のマッピングをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="a137a-148">Your IT department can export a similar mapping from your on-premises Active Directory Domain Services.</span></span>

         ![Azure AD 電子メール アドレスの AX 2012 ユーザーのマッピングを含む CSV ファイル](media/userToAzureADEmailAddressMapping.png)

     2. <span data-ttu-id="a137a-150">ファイルが準備できたら、**ファイルからのインポート**をクリックし、ファイルを参照してインポートします。</span><span class="sxs-lookup"><span data-stu-id="a137a-150">After the file is ready, click **Import from file**, browse to the file, and import it.</span></span>

        <span data-ttu-id="a137a-151">グリッドには、ファイルで指定したマッピングを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a137a-151">The grid should be filled with the mappings that you specified in the file.</span></span>

<span data-ttu-id="a137a-152">インポートされたファイルには無効なエントリが含まれている場合は、エラー ファイルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="a137a-152">If the imported file contains an entry that isn’t valid, an error file is generated.</span></span>

## <a name="validate-baseline-version"></a><span data-ttu-id="a137a-153">ベースライン バージョンの検証</span><span class="sxs-lookup"><span data-stu-id="a137a-153">Validate baseline version</span></span>

<span data-ttu-id="a137a-154">現在のバージョンをアップグレードできることを検証するには、このタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="a137a-154">Run this task to validate that the current version can be upgraded.</span></span>

- <span data-ttu-id="a137a-155">Finance and Operations のデータ アップグレード チェックリストで、**ベースライン バージョンの検証**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a137a-155">In the Finance and Operations data upgrade checklist, click **Validate baseline version**.</span></span>

<span data-ttu-id="a137a-156">ベースライン バージョンがサポートされているベースライン バージョンのいずれかの場合は、タスクは完了としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="a137a-156">If the baseline version is one of the supported baseline versions, the task is marked as completed.</span></span>


## <a name="archive-retail-salt-data"></a><span data-ttu-id="a137a-157">小売 salt データのアーカイブ</span><span class="sxs-lookup"><span data-stu-id="a137a-157">Archive retail salt data</span></span>

<span data-ttu-id="a137a-158">このタスクは、RetailSaltUtility が使用するレジストリ キーを移行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a137a-158">This task is used to migrate the registry key that RetailSaltUtility uses.</span></span> <span data-ttu-id="a137a-159">このツールは、チャンネル ユーザーの認証に使用されるハッシュに顧客が特定のランダム値を挿入する場所である、いくつかの配置に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="a137a-159">This tool is used for some deployments where the customer wants to inject a specific random value into the hash that is used to authenticate channel users.</span></span>

- <span data-ttu-id="a137a-160">Finance and Operations のデータ アップグレード チェックリストで、**小売 salt データのアーカイブ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a137a-160">In the Finance and Operations data upgrade checklist, click **Archive retail salt data**.</span></span>

<span data-ttu-id="a137a-161">プロセスが正常に行われた場合は、タスクは完了としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="a137a-161">If the process is successful, the task is marked as completed.</span></span>

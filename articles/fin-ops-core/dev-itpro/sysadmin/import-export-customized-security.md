---
title: データ管理を使用してカスタマイズしたセキュリティ コンフィギュレーションをインポート/エクスポートする
description: このトピックでは、データ管理フレームワークを使用して、カスタマイズしたセキュリティ コンフィギュレーションを環境間でエクスポートおよびインポートする方法について説明します。
author: tonyafehr
manager: Peakerbl
ms.date: 07/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 212c7fddcf670451244cc662fe75ffe77939602f
ms.sourcegitcommit: f62c2151be477acfaeace73878471abb9b1b832d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "3602544"
---
# <a name="import-or-export-a-customized-security-configuration-by-using-data-management"></a><span data-ttu-id="a2353-103">データ管理を使用してカスタマイズしたセキュリティ コンフィギュレーションをインポート/エクスポートする</span><span class="sxs-lookup"><span data-stu-id="a2353-103">Import or export a customized security configuration by using Data management</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a2353-104">このトピックでは、 [データ管理フレームワーク](../data-entities/data-entities-data-packages.md) を使用して、カスタマイズしたセキュリティ コンフィギュレーションを環境間でエクスポートおよびインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a2353-104">The topic explains how a customized security configuration can be exported and imported across environments by using the [Data management framework](../data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="a2353-105">この機能は、たとえば、カスタマイズしたセキュリティ コンフィギュレーションをテスト環境から運用環境に移動する必要がある場合などに使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2353-105">This functionality can be used when, for example, a customized security configuration must be moved from a test environment to a production environment.</span></span>

<span data-ttu-id="a2353-106">次のエンティティには、セキュリティ コンフィギュレーションを使用して追加または変更された、カスタマイズされたロールベースのセキュリティ (権限、職務権限、およびロール) を保持します。</span><span class="sxs-lookup"><span data-stu-id="a2353-106">The following entities hold the customized, role-based security (that is, privileges, duties, and roles) that has been added or modified by using security configuration:</span></span>

- <span data-ttu-id="a2353-107">セキュリティ権限のメタデータのカスタマイズ エンティティ</span><span class="sxs-lookup"><span data-stu-id="a2353-107">Security privilege metadata customization entity</span></span>
- <span data-ttu-id="a2353-108">セキュリティ職務権限のメタデータのカスタマイズ エンティティ</span><span class="sxs-lookup"><span data-stu-id="a2353-108">Security duty metadata customization entity</span></span>
- <span data-ttu-id="a2353-109">セキュリティ ロールのメタデータのカスタマイズ エンティティ</span><span class="sxs-lookup"><span data-stu-id="a2353-109">Security role metadata customization entity</span></span>

## <a name="export-customized-security-configuration"></a><span data-ttu-id="a2353-110">カスタマイズしたセキュリティ コンフィギュレーションのエクスポート</span><span class="sxs-lookup"><span data-stu-id="a2353-110">Export customized security configuration</span></span>

1. <span data-ttu-id="a2353-111"> **システム管理 \> ワークスペース \> データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2353-111">Go to **System administration \> Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="a2353-112">**エクスポート** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-112">Select the **Export** tile.</span></span>
3. <span data-ttu-id="a2353-113">**グループ名** フィールドに、グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2353-113">In the **Group name** field, enter a name for the group.</span></span>
4. <span data-ttu-id="a2353-114">**データ パッケージの生成**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a2353-114">Set the **Generate data package** option to **Yes**.</span></span>

    ![データ パッケージの生成オプションを設定](media/cb4da5cdf487ee4c55f931f1e220cdf9.png)

5. <span data-ttu-id="a2353-116">**複数追加**をクリックして、ドロップダウン ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="a2353-116">Select **Add multiple** to open the drop-down dialog box.</span></span>
6. <span data-ttu-id="a2353-117">次のフィールドを設定して、エンティティをフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="a2353-117">Filter the entities by setting the following fields:</span></span>

    - <span data-ttu-id="a2353-118">**エンティティ** フィールドに、**セキュリティ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="a2353-118">In the **Entities** field, enter **Security**.</span></span>
    - <span data-ttu-id="a2353-119">**エンティティ カテゴリ** フィールドで、**マスター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-119">In the **Entity category** field, select **Master**.</span></span>

7. <span data-ttu-id="a2353-120">**ターゲット データ形式**フィールドで、**Excel** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-120">In the **Target data format** field, select **Excel**.</span></span>
8. <span data-ttu-id="a2353-121">適用できるセキュリティのカスタマイズ エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-121">Select the applicable security customization entities.</span></span>
9. <span data-ttu-id="a2353-122">**選択対象の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-122">Select **Add selected**.</span></span>

    <span data-ttu-id="a2353-123">バージョン 10.0.12 以降では、データの長さに関する警告メッセージは無視してください。</span><span class="sxs-lookup"><span data-stu-id="a2353-123">In version 10.0.12 and later, ignore any warning messages about data length.</span></span> <span data-ttu-id="a2353-124">これらのメッセージは、データ パッケージ モードのコンテナーを使用するエンティティに含まれているため、適用されません。</span><span class="sxs-lookup"><span data-stu-id="a2353-124">Those messages aren't applicable, because the entities that are included use containers in data package mode.</span></span>

10. <span data-ttu-id="a2353-125">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-125">Select **Close**.</span></span>
11. <span data-ttu-id="a2353-126">**シーケンス** フィールドがエンティティの依存関係の順序で設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a2353-126">Make sure that the **Sequence** field is set in the order of the entity dependencies.</span></span> <span data-ttu-id="a2353-127">最初に権限、次に職務、最後にロールに指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2353-127">Privileges should be first, then duties, and finally roles.</span></span>
12. <span data-ttu-id="a2353-128">**エクスポート** の選択</span><span class="sxs-lookup"><span data-stu-id="a2353-128">Select **Export**.</span></span>
13. <span data-ttu-id="a2353-129">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-129">Select **Close**.</span></span>
14. <span data-ttu-id="a2353-130">職務が完了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="a2353-130">Wait for the job to be completed.</span></span> <span data-ttu-id="a2353-131">**更新**を選択し、ステータスを表示します。</span><span class="sxs-lookup"><span data-stu-id="a2353-131">Select **Refresh** to view the status.</span></span>
15. <span data-ttu-id="a2353-132">**ダウンロード パッケージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-132">Select **Download package**.</span></span>
16. <span data-ttu-id="a2353-133">パッケージを保存します。</span><span class="sxs-lookup"><span data-stu-id="a2353-133">Save the package.</span></span>

## <a name="import-customized-security-configuration"></a><span data-ttu-id="a2353-134">カスタマイズしたセキュリティ コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="a2353-134">Import customized security configuration</span></span>

1. <span data-ttu-id="a2353-135"> **システム管理 \> ワークスペース \> データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2353-135">Go to **System administration \> Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="a2353-136">**インポート** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-136">Select the **Import** tile.</span></span>
3. <span data-ttu-id="a2353-137">**グループ名** フィールドに、グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2353-137">In the **Group name** field, enter a name for the group.</span></span>
4. <span data-ttu-id="a2353-138">**ファイルの追加** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="a2353-138">Select **Add file**.</span></span>
5. <span data-ttu-id="a2353-139">**アップロードおよび追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-139">Select **Upload and add**.</span></span>
6. <span data-ttu-id="a2353-140">エクスポートしたパッケージを検索し、**開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-140">Find the exported package, and then select **Open**.</span></span>

    <span data-ttu-id="a2353-141">バージョン 10.0.12 以降では、データの長さに関する警告メッセージは無視してください。</span><span class="sxs-lookup"><span data-stu-id="a2353-141">In version 10.0.12 and later, ignore any warning messages about data length.</span></span> <span data-ttu-id="a2353-142">これらのメッセージは、データ パッケージ モードのコンテナーを使用するエンティティに含まれているため、適用されません。</span><span class="sxs-lookup"><span data-stu-id="a2353-142">Those messages aren't applicable, because the entities that are included use containers in data package mode.</span></span>

7. <span data-ttu-id="a2353-143">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-143">Select **Close**.</span></span>
8. <span data-ttu-id="a2353-144">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-144">Select **Import**.</span></span>
9. <span data-ttu-id="a2353-145">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2353-145">Select **Close**.</span></span>
10. <span data-ttu-id="a2353-146">職務が完了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="a2353-146">Wait for the job to be completed.</span></span> <span data-ttu-id="a2353-147">**更新**を選択し、ステータスを表示します。</span><span class="sxs-lookup"><span data-stu-id="a2353-147">Select **Refresh** to view the status.</span></span>

## <a name="related-security-configuration-entities"></a><span data-ttu-id="a2353-148">関連するセキュリティ コンフィギュレーション エンティティ</span><span class="sxs-lookup"><span data-stu-id="a2353-148">Related security configuration entities</span></span>

- <span data-ttu-id="a2353-149">**SystemSecurityUserRoleOrganizationEntity** – セキュリティロールに組織を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a2353-149">**SystemSecurityUserRoleOrganizationEntity** – Assignment of organizations to security roles.</span></span>
- <span data-ttu-id="a2353-150">**職務のセキュリティ分掌ルール** – 職務分掌ルール。</span><span class="sxs-lookup"><span data-stu-id="a2353-150">**Security segregation of duties rule** – Segregation of duties rules.</span></span>
- <span data-ttu-id="a2353-151">**職務のセキュリティ分掌競合** – 職務分掌競合。</span><span class="sxs-lookup"><span data-stu-id="a2353-151">**Security segregation of duties conflict** – Segregation of duties conflicts.</span></span> <span data-ttu-id="a2353-152">このエンティティには未解決の競合がありますが、競合も確認されています。</span><span class="sxs-lookup"><span data-stu-id="a2353-152">This entity has unresolved conflicts but also reviewed conflicts.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2353-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a2353-153">Additional resources</span></span>

- [<span data-ttu-id="a2353-154">データ インポート/エクスポート ジョブの概要</span><span class="sxs-lookup"><span data-stu-id="a2353-154">Data import and export jobs overview</span></span>](../data-entities/data-import-export-job.md)
- <span data-ttu-id="a2353-155">Andr&eacute; Arnaud de Calavon で、[データ エンティティ (ブログの投稿) を含むすべてのユーザーおよびセキュリティ設定の移動](https://dynamicspedia.com/2020/05/move-all-user-and-security-settings-with-data-entities/)</span><span class="sxs-lookup"><span data-stu-id="a2353-155">[Move all user and security settings with data entities (blog post)](https://dynamicspedia.com/2020/05/move-all-user-and-security-settings-with-data-entities/), by Andr&eacute; Arnaud de Calavon</span></span>

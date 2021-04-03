---
title: ER 移行クリーンアップ
description: このトピックでは、ER 移行クリーンアップ機能を使用して ER テンプレートに関する問題を解決する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: b09afc30c401e2dccfc4114261dc5e713c8c470c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565518"
---
# <a name="er-migration-cleanup"></a><span data-ttu-id="6e2d3-103">ER 移行クリーンアップ</span><span class="sxs-lookup"><span data-stu-id="6e2d3-103">ER migration cleanup</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6e2d3-104">Finance インスタンスを管理する場合、現在のインスタンスを別の場所に移行する必要性が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-104">When you manage your Finance instances, you might decide to migrate your current instance to another location.</span></span> <span data-ttu-id="6e2d3-105">たとえば、本番インスタンスを新しいサンドボックス環境に移行するかもしれません。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-105">For example, you might migrate your production instance to a new sandbox environment.</span></span> <span data-ttu-id="6e2d3-106">テンプレートを Microsoft Azure Blob ストレージに保存するように電子レポート（ER）フレームワークを構成した場合、新しいサンドボックス環境の **DocuValue** テーブルは、本番環境の Blob ストレージのインスタンスを参照します。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-106">If you configured the Electronic reporting (ER) framework to store templates in Microsoft Azure Blob storage, the **DocuValue** table in the new sandbox environment refers to the instance of Blob storage in the production environment.</span></span> <span data-ttu-id="6e2d3-107">ただし、移行プロセスでは、Blob ストレージ内のアーティファクトの移行に対応していないため、このインスタンスにはサンドボックス環境からアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-107">However, this instance can't be accessed from the sandbox environment because the migration process doesn't support the migration of artifacts in Blob storage.</span></span> <span data-ttu-id="6e2d3-108">新しいサンドボックス環境では、まだ ER のテンプレートを取得していないサンドボックス環境の Blob ストレージのインスタンスを参照することが予想されます。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-108">Rather, it's expected that in the new sandbox environment, you refer to the instance of Blob storage in the sandbox environment that does not yet obtain the ER templates.</span></span>

<span data-ttu-id="6e2d3-109">したがって、テンプレートを使用して ER 形式を実行してビジネス ドキュメントを生成すると、例外が発生し、テンプレートが欠落していることが通知されます。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-109">If you try to run an ER format that uses a template to generate business documents, an exception occurs, and you're notified about the missing template.</span></span> <span data-ttu-id="6e2d3-110">また、ER 移行クリーンアップ オプションを使用して、テンプレートを含む ER 形式の構成を削除してから再インポートする方法も紹介しています。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-110">You're also guided to use the ER migration cleanup option to delete and then re-import the ER format configuration that contains the template.</span></span>

<span data-ttu-id="6e2d3-111">[![ER 形式の実行](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)</span><span class="sxs-lookup"><span data-stu-id="6e2d3-111">[![Running an ER format](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)</span></span>

<span data-ttu-id="6e2d3-112">**構成** ページ（**組織管理の** \> **電子レポートの構成** \> **構成**）に移動し、構成ツリーでテンプレートを使用したER 形式の構成を削除しようとした際には、同様のエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-112">You will receive a similar error if you navigate to the **Configurations** page (**Organization administration** \> **Electronic reporting** \> **Configurations**) and in the configurations tree, try to delete an ER format configuration that uses a template.</span></span>

<span data-ttu-id="6e2d3-113">[![ER 形式の削除](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)</span><span class="sxs-lookup"><span data-stu-id="6e2d3-113">[![Deletion an ER format](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)</span></span>

<span data-ttu-id="6e2d3-114">アクセスできない ER テンプレートの問題を解決するには、次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-114">Complete the following steps to resolve issues with ER templates that you are unable to access.</span></span>

1.  <span data-ttu-id="6e2d3-115">**組織管理** \> **定期** \> **移行クリーンアップ** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-115">Go to **Organization administration** \> **Periodic** \> **Migration cleanup** page.</span></span>
2.  <span data-ttu-id="6e2d3-116">実行、削除できない ER 形式の構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-116">Select an ER format configuration that can’t be executed or deleted.</span></span>
3.  <span data-ttu-id="6e2d3-117">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-117">Select **Delete**.</span></span>
4.  <span data-ttu-id="6e2d3-118">選択したER形式の構成の削除を確認します。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-118">Confirm the deletion of the selected ER format configuration.</span></span>
5.  <span data-ttu-id="6e2d3-119">削除された ER 形式の構成を現在の Finance インスタンスを [インポート](download-electronic-reporting-configuration-lcs.md) します。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-119">[Import](download-electronic-reporting-configuration-lcs.md) the deleted ER format configuration to the current Finance instance.</span></span>

## <a name="applicability"></a><span data-ttu-id="6e2d3-120">適合性</span><span class="sxs-lookup"><span data-stu-id="6e2d3-120">Applicability</span></span>

> <span data-ttu-id="6e2d3-121">[重要] **移行クリーンアップ** オプションは、 アクセスできない ER テンプレートを含む ER 形式の構成のみを対象としています。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-121">[Important] The **Migration cleanup** option is targeted only for ER format configurations that contain non-accessible ER templates.</span></span> <span data-ttu-id="6e2d3-122">**移行クリーンアップ** オプションを使用して ER 形式の構成を削除すると、ER はアプリケーション データベース内の構成アーティファクトのみに関連しているテンプレートを削除します。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-122">When you delete an ER format configuration by using the **Migration cleanup** option, ER deletes the templates that are related to the configuration artifacts in the only application database.</span></span> <span data-ttu-id="6e2d3-123">Blob ストレージに適切な物理ファイルが存在するかどうかの検証はされません。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-123">The existence of the appropriate physical files in Blob storage are not validated.</span></span> <span data-ttu-id="6e2d3-124">ここではむしろ存在しないことが前提となっています。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-124">Instead, it is assumed that there are none.</span></span> <span data-ttu-id="6e2d3-125">したがって、**構成** ページの ER 設定削除オプションの代わりに **移行クリーンアップ** オプション使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-125">Therefore, do not use the **Migration cleanup** option as an alternative to the ER configuration deletion option on the **Configurations** page.</span></span> <span data-ttu-id="6e2d3-126">**移行クリーンアップ** オプションは、**構成** ページの ER 設定削除オプションが失敗した場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-126">Use the **Migration cleanup** option only when the ER configuration deletion option on the **Configurations** page failed.</span></span>
>
> <span data-ttu-id="6e2d3-127">参照されたテンプレートが Blob ストレージで利用可能な場合に ER 形式の構成を削除する目的で **移行クリーンアップ**  オプションを使用すると、アプリケーション データベース内の関連する構成アーティファクトのみが削除されます。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-127">If you use the **Migration cleanup** option to delete an ER format configuration when the referred template is available in the Blob storage, you only delete related configuration artifacts in the application database.</span></span> <span data-ttu-id="6e2d3-128">Blob ストレージのテンプレートの物理ファイルは残ります。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-128">The physical file of the template in the Blob storage remains.</span></span> <span data-ttu-id="6e2d3-129">Blob ストレージにおけるファイルの上書きは許可されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-129">File overwriting in Blob storage is no longer allowed.</span></span> <span data-ttu-id="6e2d3-130">詳細については、[KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-130">For more information, see [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217).</span></span> <span data-ttu-id="6e2d3-131">また、この環境で移行のクリーンアップを使用して削除した構成を再度インポートすることもできなくなります。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-131">Additionally, you will no longer be able to re-import the configurations deleted by using the Migration cleanup in this environment.</span></span> <span data-ttu-id="6e2d3-132">この問題を解決するには、対応するファイルを Blob ストレージで検索し、手動で削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-132">To resolve this issue, you need to find the corresponding file in Blob storage and manually delete it.</span></span>

<span data-ttu-id="6e2d3-133">[![ER 形式のインポート](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)</span><span class="sxs-lookup"><span data-stu-id="6e2d3-133">[![Importing an ER format](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)</span></span>

<span data-ttu-id="6e2d3-134">アプリケーション インスタンスを移行対象として複数回使用されている場所に移行した場合で、Blob ストレージに ER のテンプレート ファイルがすでに含まれている場合にも、同様の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-134">A similar issue may occur if you migrate your application instance to another location that has been used as a migration target more than once and for which the Blob storage already contains ER template files.</span></span>

<span data-ttu-id="6e2d3-135">ER 形式の構成が複数存在する場合があるため、このプロセスには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-135">Because you can have several ER format configurations, this process can be time consuming.</span></span> <span data-ttu-id="6e2d3-136">したがって、[ER テンプレートのバックアップ ストレージ](er-backup-storage-templates.md) 機能を使用して、壊れた参照を含むテンプレートを自動的に回復することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="6e2d3-136">Therefore, using the [Backup storage of ER templates](er-backup-storage-templates.md) feature to automatically recover templates with broken references is preferred.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: 複数のワークシートを含む Excel データ エンティティ テンプレートからのデータ インポート
description: このトピックでは、Excel データ エンティティのテンプレートを使用して Microsoft Dynamics 365 for Finance and Operations にデータをインポートする方法について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 48239b48cbc24e34d74bbac36e8f827a15d7b840
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551056"
---
# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a><span data-ttu-id="8e825-103">複数のワークシートを含む Excel データ エンティティ テンプレートからのデータ インポート</span><span class="sxs-lookup"><span data-stu-id="8e825-103">Import data from Excel data entity templates that have multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e825-104">Microsoft Dynamics 365 for Finance and Operations のデータ管理は、データ エンティティ用の Microsoft Excel ベースのテンプレートをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8e825-104">Data management in Microsoft Dynamics 365 for Finance and Operations supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="8e825-105">これらのテンプレートには、1 つまたは複数のワークシートを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8e825-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="8e825-106">複数のワークシートを含むテンプレートは、1つのファイルでデータを管理し、複数のデータ エンティティにインポートすると便利な場合によく使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e825-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="8e825-107">サイトや倉庫の例があります。</span><span class="sxs-lookup"><span data-stu-id="8e825-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="8e825-108">ファイルを一度アップロードし、すべてのエンティティにマップする</span><span class="sxs-lookup"><span data-stu-id="8e825-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="8e825-109">**サイト**および**倉庫**と呼ばれるワークシートを持つ Excel ファイルが 1 つある場合の例を考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="8e825-109">Let's take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="8e825-110">データ インポート プロジェクトを設定するには、最初のデータ エンティティ、**サイト**を追加してからファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="8e825-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="8e825-111">このエンティティをしようするために**サイト**をワークシートとして選択することができます。</span><span class="sxs-lookup"><span data-stu-id="8e825-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="8e825-112">**ファイルの追加** フォームを残さずに第 2 のエンティティ **倉庫** を追加すると、ワークシートの参照により、ファイルを再度アップロードせずに **倉庫** ワークシートを選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8e825-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="8e825-113">新しいファイルをアップロードする唯一の理由は、**倉庫**のデータが他のファイルにある場合だけです。</span><span class="sxs-lookup"><span data-stu-id="8e825-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![複数のワークシート](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="8e825-115">エンティティ マッピングへのワークシートの修正</span><span class="sxs-lookup"><span data-stu-id="8e825-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="8e825-116">インポート ジョブのデータ エンティティへのワークシートのマッピングは、グリッドから固定することができます。</span><span class="sxs-lookup"><span data-stu-id="8e825-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="8e825-117">グリッドの **ワークシート** 列には、マップされたファイルのワークシートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e825-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="8e825-118">ドロップダウン メニューから別のワークシートを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="8e825-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="8e825-119">選択したワークシートがすでにデータ プロジェクト内のエンティティにマップされている場合は、変更を確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e825-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="8e825-120">グリッド内のすべてのマッピングを修正することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8e825-120">We recommend that you fix all mappings in the grid.</span></span>

![ワークシート マッピングの更新](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="8e825-122">新しいファイルに再マップします</span><span class="sxs-lookup"><span data-stu-id="8e825-122">Re-map to a new file</span></span>

<span data-ttu-id="8e825-123">同じファイルの新しいバージョンまたは完全に新しいファイルをデータ プロジェクトの既存のエンティティにアップロードする必要がある場合は、**ファイルの追加**エクスペリエンスを使用して、エンティティを最初に追加した時のように、再度追加します。</span><span class="sxs-lookup"><span data-stu-id="8e825-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="8e825-124">続行する前に、システムはデータ プロジェクト内の既存のエンティティを上書きすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8e825-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="8e825-125">再度追加されない (または上書きされた) エンティティは、以前のファイルから以前のマッピングを保持し続けます。</span><span class="sxs-lookup"><span data-stu-id="8e825-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="8e825-126">プロジェクトを実行してファイルをアップロードする</span><span class="sxs-lookup"><span data-stu-id="8e825-126">Upload a file using Run project</span></span>

<span data-ttu-id="8e825-127">**プロジェクトを実行** オプションを使用して Excel ファイルをアップロードして、インポート プロジェクトを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="8e825-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="8e825-128">データ プロジェクト内のデータ エンティティの既存のマッピングと同じワークシートを持つファイルのみをアップロードするように注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e825-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="8e825-129">新しくアップロードされたファイルにワークシートが見つからない場合、システムはエラーを表示してインポートを停止します。</span><span class="sxs-lookup"><span data-stu-id="8e825-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="8e825-130">エンティティに対してワークシートへのマッピングを変更する必要がある場合は、**プロジェクトを実行** エクスペリエンスのファイルを使用する前に、データプロジェクト内のマッピングを最初にデータプロジェクト内から更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e825-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>

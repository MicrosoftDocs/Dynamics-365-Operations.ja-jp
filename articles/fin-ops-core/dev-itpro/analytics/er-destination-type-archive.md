---
title: ER アーカイブ送信先のタイプ
description: このトピックでは、送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、アーカイブ送信先をコンフィギュレーションする方法に関する情報を提供します。
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019868"
---
# <span data-ttu-id="5e636-103"><a name="ArchiveDestinationType">アーカイブ先</a></span><span class="sxs-lookup"><span data-stu-id="5e636-103"><a name="ArchiveDestinationType">Archive destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e636-104">送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、アーカイブ送信先をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="5e636-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="5e636-105">送信先の設定に基づいて、生成されたドキュメントは ER ジョブ リストのレコードの添付ファイルとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="5e636-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="5e636-106">このオプションを使用して、生成したドキュメントを Microsoft SharePoint フォルダーまたは Microsoft Azure ストレージに送信することができます。</span><span class="sxs-lookup"><span data-stu-id="5e636-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="5e636-107">**有効** を **はい** に設定し、選択したドキュメント タイプで定義されている変換先に出力を送信します。</span><span class="sxs-lookup"><span data-stu-id="5e636-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="5e636-108">グループが**ファイル**に設定されているドキュメントタイプのみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="5e636-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="5e636-109">**組織管理** \> **ドキュメント管理** \> **ドキュメント タイプ**で、ドキュメント [タイプ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) を定義します。</span><span class="sxs-lookup"><span data-stu-id="5e636-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="5e636-110">電子申告の送信先への構成は、ドキュメント管理システムの構成と同じです。</span><span class="sxs-lookup"><span data-stu-id="5e636-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="5e636-111">[![ドキュメント タイプ ページ](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="5e636-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="5e636-112">場所は、ファイルの保存場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="5e636-112">The location determines where the file is saved.</span></span> <span data-ttu-id="5e636-113">**アーカイブ**先を有効にすると、結果をジョブ アーカイブに保存できます。</span><span class="sxs-lookup"><span data-stu-id="5e636-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="5e636-114">結果は、**組織管理** \> **電子申告** \> **電子申告アーカイブ済ジョブ** で表示できます。</span><span class="sxs-lookup"><span data-stu-id="5e636-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="5e636-115">ジョブ アーカイブのドキュメント タイプは、**組織管理** \> **ワークスペース** \> **電子申告** \> **電子申告のパラメーター**に移動して選択します。</span><span class="sxs-lookup"><span data-stu-id="5e636-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="5e636-116">詳細については、[電子申告 (ER) フレームワークのコンフィギュレーション](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e636-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="5e636-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="5e636-117">SharePoint</span></span>

<span data-ttu-id="5e636-118">指定された SharePoint フォルダーにファイルを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="5e636-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="5e636-119">既定の SharePoint サーバーを定義するには、**組織管理** \> **ドキュメント管理** \> **ドキュメント管理パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="5e636-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="5e636-120">**SharePoint** タブで、SharePoint フォルダーをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="5e636-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="5e636-121">ER 出力を保存するフォルダーとして選択できます。</span><span class="sxs-lookup"><span data-stu-id="5e636-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="5e636-122">**SharePoint** の場所は、このドキュメント タイプで選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e636-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="5e636-123">[![SharePoint フォルダーの選択](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="5e636-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="5e636-124">Azure ストレージ</span><span class="sxs-lookup"><span data-stu-id="5e636-124">Azure Storage</span></span>

<span data-ttu-id="5e636-125">ドキュメント タイプの場所を **Azure ストレージ**に設定すると、Azure ストレージにファイルを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="5e636-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e636-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5e636-126">Additional resources</span></span>

- [<span data-ttu-id="5e636-127">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="5e636-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="5e636-128">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="5e636-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="5e636-129">ドキュメント管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5e636-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)

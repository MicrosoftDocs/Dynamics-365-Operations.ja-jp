---
title: ER アーカイブ送信先のタイプ
description: このトピックでは、電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対してアーカイブ送信先を構成する方法について説明します。
author: NickSelin
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 079eda04fcc41fc637419a83452db10b89ed1ab9
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894031"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="96832-103">ER アーカイブ送信先のタイプ</span><span class="sxs-lookup"><span data-stu-id="96832-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96832-104">送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各 **フォルダー** または **ファイル** コンポーネントに対して、アーカイブ送信先をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="96832-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="96832-105">送信先の設定に基づいて、生成されたドキュメントは ER ジョブ リストのレコードの添付ファイルとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="96832-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="96832-106">結果を表示するには、**組織管理** \> **電子申告** \> **電子申告ジョブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="96832-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="96832-107">このオプションを使用して、生成したドキュメントを Microsoft SharePoint フォルダーまたは Microsoft Azure ストレージに送信することができます。</span><span class="sxs-lookup"><span data-stu-id="96832-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="96832-108">**有効** を **はい** に設定し、選択したドキュメント タイプで定義されている変換先に出力を送信します。</span><span class="sxs-lookup"><span data-stu-id="96832-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="96832-109">グループが **ファイル** に設定されているドキュメントタイプのみ選択できます。</span><span class="sxs-lookup"><span data-stu-id="96832-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="96832-110">**組織管理** \> **ドキュメント管理** \> **ドキュメント タイプ** で、ドキュメント [タイプ](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) を定義します。</span><span class="sxs-lookup"><span data-stu-id="96832-110">You define document [types](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="96832-111">電子申告の送信先への構成は、ドキュメント管理システムの構成と同じです。</span><span class="sxs-lookup"><span data-stu-id="96832-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="96832-112">[![ドキュメント タイプ ページ](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="96832-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="96832-113">場所は、ファイルの保存場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="96832-113">The location determines where the file is saved.</span></span> <span data-ttu-id="96832-114">**アーカイブ** 先を有効にすると、結果をジョブ アーカイブに保存できます。</span><span class="sxs-lookup"><span data-stu-id="96832-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="96832-115">結果は、**組織管理** \> **電子申告** \> **電子申告アーカイブ済ジョブ** で表示できます。</span><span class="sxs-lookup"><span data-stu-id="96832-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="96832-116">ジョブ アーカイブのドキュメント タイプは、**組織管理** \> **ワークスペース** \> **電子申告** \> **電子申告のパラメーター** に移動して選択します。</span><span class="sxs-lookup"><span data-stu-id="96832-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="96832-117">詳細については、[電子申告 (ER) フレームワークのコンフィギュレーション](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96832-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="96832-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="96832-118">SharePoint</span></span>

<span data-ttu-id="96832-119">指定された SharePoint フォルダーにファイルを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="96832-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="96832-120">既定の SharePoint サーバーを定義するには、**組織管理** \> **ドキュメント管理** \> **ドキュメント管理パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="96832-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="96832-121">**SharePoint** タブで、SharePoint フォルダーをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="96832-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="96832-122">ER 出力を保存するフォルダーとして選択できます。</span><span class="sxs-lookup"><span data-stu-id="96832-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="96832-123">**SharePoint** の場所は、このドキュメント タイプで選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96832-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="96832-124">[![SharePoint フォルダーの選択](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="96832-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="96832-125">Azure ストレージ</span><span class="sxs-lookup"><span data-stu-id="96832-125">Azure Storage</span></span>

<span data-ttu-id="96832-126">ドキュメント タイプの場所を **Azure ストレージ** に設定すると、Azure ストレージにファイルを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="96832-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="96832-127">ER フレームワークは、処理する必要があるドキュメントに対して、7 日間の保持ポリシーを適用するデータ管理フレームワークとは異なり、Azure Blob Storage にファイルを永久に保存します。</span><span class="sxs-lookup"><span data-stu-id="96832-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="96832-128">詳細については、[メッセージ状態を取得中の API](../data-entities/recurring-integrations.md#api-for-getting-message-status) および [ステータス チェック API](../data-entities/data-management-api.md#status-check-api) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96832-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="96832-129">ER 関連のファイルは、必要な限り、アプリケーション テーブル レコードの添付ファイルとし、Azure Blob Storage に保存されます。</span><span class="sxs-lookup"><span data-stu-id="96832-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="96832-130">1 つのファイルが、このファイルが関連付けられているアプリケーション テーブル レコードと共に、Azure Blob Storage から削除されます。</span><span class="sxs-lookup"><span data-stu-id="96832-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96832-131">追加リソース</span><span class="sxs-lookup"><span data-stu-id="96832-131">Additional resources</span></span>

- [<span data-ttu-id="96832-132">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="96832-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="96832-133">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="96832-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="96832-134">ドキュメント管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="96832-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
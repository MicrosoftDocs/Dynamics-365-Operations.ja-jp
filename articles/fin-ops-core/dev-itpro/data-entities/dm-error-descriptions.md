---
title: データ管理エラーの説明
description: このトピックでは、データ管理で発生する可能性があるエラー メッセージについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-09-15
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: de55489d0bc5be9f57b6882211607c1fbf5eb4ba
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685679"
---
# <a name="data-management-error-descriptions"></a><span data-ttu-id="54b3b-103">データ管理エラーの説明</span><span class="sxs-lookup"><span data-stu-id="54b3b-103">Data management error descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54b3b-104">このトピックでは、特定のエラーが表示されるときのシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="54b3b-104">This topic documents the scenarios when a specific error will be seen.</span></span> <span data-ttu-id="54b3b-105">これらのシナリオは、エラーとシナリオの完全な一覧ではありませんが、このリストは継続的に更新されるため、最新情報をチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="54b3b-105">These scenarios aren't a complete list of errors and scenarios, however this list will be continuously updated so keep checking back for updates.</span></span> <span data-ttu-id="54b3b-106">特定のエラーが扱われるべきかどうかに関するこのページのフィードバックをお送りください。</span><span class="sxs-lookup"><span data-stu-id="54b3b-106">Any feedback on this page with regards to specific errors that should be covered are welcome.</span></span>

<span data-ttu-id="54b3b-107">このトピックでは、データ管理で発生する可能性があるエラー メッセージについて説明します。</span><span class="sxs-lookup"><span data-stu-id="54b3b-107">This topic describes the error messages that you might encounter in data management.</span></span>

## <a name="import-to-target-failed-due-to-an-update-conflict-as-more-than-one-process-is-trying-to-update-the-same-record-at-the-same-time"></a><span data-ttu-id="54b3b-108">複数のプロセスとしての更新競合のために失敗したターゲットへのインポートが、同じレコードを同時に更新しようとしている</span><span class="sxs-lookup"><span data-stu-id="54b3b-108">Import to target failed due to an update conflict as more than one process is trying to update the same record at the same time</span></span>

<span data-ttu-id="54b3b-109">定期的なインポート (API をキューに入れる) を使用するとき、頻度の高いのエンドポイントにファイルが送信され、連続したメッセージの処理が有効になっていない場合、データ管理は同時にファイルを処理しようとします。</span><span class="sxs-lookup"><span data-stu-id="54b3b-109">When you use recurring imports (enqueue API), if the files are sent to the end point at high frequency and the sequential processing of messages isn't enabled, data management will try to process the files in parallel.</span></span> <span data-ttu-id="54b3b-110">ファイルが並行で処理され、複数のファイルが同一のレコードを持つ場合、複数のスレッドが同時に同じレコードを更新しようとします。</span><span class="sxs-lookup"><span data-stu-id="54b3b-110">When files are processed in parallel, and multiple files have the same record, multiple threads will try to update the same record at the same time.</span></span> <span data-ttu-id="54b3b-111">これがデータの問題である場合、ファイルの間で同じレコードが繰り返さないように、データを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54b3b-111">If this is a data issue, you must update the data so that the same records don’t repeat across files.</span></span> <span data-ttu-id="54b3b-112">これがデータの問題ではなく、エンティティがこのようなケースを処理すると予測される場合は、バグの可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54b3b-112">If this is not a data issue and the entity is expected to handle such cases, this might be a bug.</span></span> <span data-ttu-id="54b3b-113">不具合の場合、問題を軽減するため、順番にファイルを処理することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="54b3b-113">For bugs, to mitigate the issue, you can choose to sequentially process the files.</span></span> <span data-ttu-id="54b3b-114">これがデータの問題ではなく、エンティティが並行処理することが予想されない場合、このエンティティが並列処理の対象でない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54b3b-114">If this is not a data issue and the entity is not expected to process in parallel, then this entity must not be subjected to parallel processing.</span></span> <span data-ttu-id="54b3b-115">定期的なジョブ内のメッセージの連続した処理を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="54b3b-115">You should enable sequential processing of messages in the recurring job.</span></span>

## <a name="there-are-fields-which-are-not-mapped-to-entity-entityname"></a><span data-ttu-id="54b3b-116">エンティティ \<EntityName\> にマップされていないフィールドがあります</span><span class="sxs-lookup"><span data-stu-id="54b3b-116">There are field(s) which are not mapped to Entity \<EntityName\></span></span>

<span data-ttu-id="54b3b-117">一般的には、後でインポートに使用できるエンティティ テンプレート ファイルを生成するためにエクスポート機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="54b3b-117">It is a common practice to use the export functionality to generate the entity template file that can be later used for imports.</span></span> <span data-ttu-id="54b3b-118">ただし、"最初の行ヘッダー" が "いいえ" になっている固定長形式でテンプレートをエクスポートしますが (設定されたソース データ形式で)、エクスポートしたテンプレートには列の名前がありません。</span><span class="sxs-lookup"><span data-stu-id="54b3b-118">However, while exporting the template, in fixed width format with 'First row header' set to 'No' (in source data formats set up), the exported template will not have the column names.</span></span> <span data-ttu-id="54b3b-119">このファイルのインポート時、このエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="54b3b-119">When this file is imported, it will result in this error.</span></span> 

## <a name="data-package-download---error-downloading-data-package-for-job--record-for-id---guid-not-found"></a><span data-ttu-id="54b3b-120">データ パッケージ ダウンロード - ジョブ '' のデータ パッケージのダウンロード エラーです。</span><span class="sxs-lookup"><span data-stu-id="54b3b-120">Data package download - Error downloading data package for job ''.</span></span> <span data-ttu-id="54b3b-121">ID - {GUID} のレコードが見つかりません</span><span class="sxs-lookup"><span data-stu-id="54b3b-121">Record for ID - {GUID} not found</span></span>

<span data-ttu-id="54b3b-122">このエラーが発生するシナリオの 1 つは、開発環境などの環境が UAT などの別の環境にあるデータベースをポイントしており、エクスポート ジョブがソース環境から実行される場合などです。</span><span class="sxs-lookup"><span data-stu-id="54b3b-122">One of the scenarios where this error can happen is when the environment, such as the dev environment, points to the database in another environment, such as UAT, and the export job is run from the source environment.</span></span> <span data-ttu-id="54b3b-123">この例では、開発です。</span><span class="sxs-lookup"><span data-stu-id="54b3b-123">which is dev in this example.</span></span> <span data-ttu-id="54b3b-124">エクスポートしたファイルは、ソース環境 (この例では開発) に関連付けられている blob ストレージにアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="54b3b-124">The exported file gets uploaded to the blob storage that is associated with the source environment (dev, in this example).</span></span> <span data-ttu-id="54b3b-125">ただし、データベースが共有されているため、このジョブはターゲット環境 (UAT) にも表れます。</span><span class="sxs-lookup"><span data-stu-id="54b3b-125">However, this job will also show up in the target environment (UAT) since the database is shared.</span></span> <span data-ttu-id="54b3b-126">**ファイルのダウンロード** オプションを使用してエクスポートしたファイルをダウンロードしようとする場合、ダウンロード元となるターゲット環境 (UAT) の Blob ストレージにファイルが存在しないために、このエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="54b3b-126">If you try to download the exported file using the **Download file** option, this error will display because the file does not exist in the blob storage of the target environment (UAT) from where you are trying to download.</span></span>

## <a name="xml-is-not-in-correct-format-exception-from-hresult-0xc0010009"></a><span data-ttu-id="54b3b-127">XML が正しい形式ではありません-HRESULT: 0xC0010009 からの例外</span><span class="sxs-lookup"><span data-stu-id="54b3b-127">XML is not in correct format-Exception from HRESULT: 0xC0010009</span></span>

<span data-ttu-id="54b3b-128">このメッセージは、ファイルにおける XML 形式のすべての問題をカバーします。</span><span class="sxs-lookup"><span data-stu-id="54b3b-128">This message covers all XML formatting issues in the file.</span></span> <span data-ttu-id="54b3b-129">たとえば、データ プロジェクトには、操作に使用されているファイルに存在しない列のマッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="54b3b-129">For example, the data project has mappings for columns that do not exist in the file that is being used for the operation.</span></span> <span data-ttu-id="54b3b-130">このエラーは、ファイルから特定の列が削除され、このファイルが使用される場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54b3b-130">This error can happen if certain columns were removed from the file and this file is now used.</span></span> <span data-ttu-id="54b3b-131">データ プロジェクトでマッピングを修正するか、すべての列が正常に存在するようにファイルを修正します。</span><span class="sxs-lookup"><span data-stu-id="54b3b-131">Either fix the mapping in the data project or fix the file to have all the columns as expected.</span></span>

## <a name="error-while-uploading-a-file-during-export"></a><span data-ttu-id="54b3b-132">エクスポート時のファイルのアップロード中にエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="54b3b-132">Error while uploading a file during export</span></span>

<span data-ttu-id="54b3b-133">開発環境でエクスポート処理をした際に、エクスポートファイルのアップロードができない旨のエラーが発生する。</span><span class="sxs-lookup"><span data-stu-id="54b3b-133">When running an export on a development environment, an error could occur relating to not being able to upload the export file.</span></span> <span data-ttu-id="54b3b-134">これは、Azure Storage エミュレーターが使用できないか、旧バージョンの エミュレーター が インストール されている場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="54b3b-134">This could occur if Azure Storage Emulator is not available or an older version of the emulator is installed.</span></span> <span data-ttu-id="54b3b-135">この問題を解決するには、最新のエミュレータをインストールし、仮想マシン (VM) を再起動の上、エクスポート ジョブを再実行してください。</span><span class="sxs-lookup"><span data-stu-id="54b3b-135">To resolve this issue, install the latest emulator, restart the virtual machine (VM), and rerun the export job.</span></span> <span data-ttu-id="54b3b-136">ストレージのエミュレーターは [Azure Storage エミュレーター](https://docs.microsoft.com/azure/storage/common/storage-use-emulator) からインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="54b3b-136">The storage emulator can be installed from [Azure Storage Emulator](https://docs.microsoft.com/azure/storage/common/storage-use-emulator).</span></span>


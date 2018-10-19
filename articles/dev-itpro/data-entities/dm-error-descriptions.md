---
title: "データ管理エラーの説明"
description: "このトピックでは、データ管理で発生する可能性があるエラー メッセージについて説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 09/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-09-15
ms.dyn365.ops.version: Platform update 20
ms.translationtype: HT
ms.sourcegitcommit: 1bf37d65cd8ce6a98fc2d2fb11ae9587cf6958a3
ms.openlocfilehash: 078adcee35af65430d31b2c41bae230b98060f3d
ms.contentlocale: ja-jp
ms.lasthandoff: 09/27/2018

---

# <a name="data-management-error-descriptions"></a><span data-ttu-id="b2e0b-103">データ管理エラーの説明</span><span class="sxs-lookup"><span data-stu-id="b2e0b-103">Data management error descriptions</span></span>
<span data-ttu-id="b2e0b-104">このトピックでは、特定のエラーが表示されるときのシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-104">This topic documents the scenarios when a specific error will be seen.</span></span> <span data-ttu-id="b2e0b-105">これはエラーとシナリオの完全な一覧ではありませんが、このリストは継続的に更新されるため、最新情報をチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-105">This is not a complete list of errors and scenarios, however this list will be continuously updated so keep checking back for updates.</span></span> <span data-ttu-id="b2e0b-106">特定のエラーが扱われるべきかどうかに関するこのページのフィードバックをお送りください。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-106">Any feedback on this page with regards to specific errors that should be covered are welcome.</span></span> <span data-ttu-id="b2e0b-107">このトピックが最新の状態になるように、フィードバック依頼を優先するよう努めます。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-107">We will strive to prioritize your feedback requests so that this topic stays up to date.</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2e0b-108">このトピックでは、データ管理で発生する可能性があるエラー メッセージについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-108">This topic describes the error messages that you might encounter in data management.</span></span>

## <a name="import-to-target-failed-due-to-an-update-conflict-as-more-than-one-process-is-trying-to-update-the-same-record-at-the-same-time"></a><span data-ttu-id="b2e0b-109">複数のプロセスとしての更新競合のために失敗したターゲットへのインポートが、同じレコードを同時に更新しようとしている</span><span class="sxs-lookup"><span data-stu-id="b2e0b-109">Import to target failed due to an update conflict as more than one process is trying to update the same record at the same time</span></span>
<span data-ttu-id="b2e0b-110">定期的なインポート (API をキューに入れる) を使用するとき、頻度の高いのエンドポイントにファイルが送信され、連続したメッセージの処理が有効になっていない場合、データ管理は同時にファイルを処理しようとします。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-110">When you use recurring imports (enqueue API), if the files are sent to the end point at high frequency and the sequential processing of messages isn't enabled, data management will try to process the files in parallel.</span></span> <span data-ttu-id="b2e0b-111">ファイルが並行で処理され、複数のファイルが同一のレコードを持つ場合、複数のスレッドが同時に同じレコードを更新しようとします。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-111">When files are processed in parallel, and multiple files have the same record, multiple threads will try to update the same record at the same time.</span></span> <span data-ttu-id="b2e0b-112">これがデータの問題である場合、ファイルの間で同じレコードが繰り返さないように、データを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-112">If this is a data issue, you must update the data so that the same records don’t repeat across files.</span></span> <span data-ttu-id="b2e0b-113">これがデータの問題ではなく、エンティティがこのようなケースを処理すると予測される場合、ファイルを順番に処理するか、ファイルがエンドポイントに送信される頻度を下げることができます。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-113">If this is not a data issue and the entity is expected to handle such cases, you can chose to sequentially process the files or reduce the frequency of which the files are sent to the end point.</span></span> <span data-ttu-id="b2e0b-114">ただし、頻度を下げる場合は、タイミングによってはこのエラーを受け取り続ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-114">However, if you reduce the frequency, you might continue to receive this error, depending on the timing.</span></span>

## <a name="there-are-fields-which-are-not-mapped-to-entity-ltentitynamegt"></a><span data-ttu-id="b2e0b-115">エンティティ &lt;EntityName&gt; にマップされていないフィールドがあります</span><span class="sxs-lookup"><span data-stu-id="b2e0b-115">There are field(s) which are not mapped to Entity &lt;EntityName&gt;</span></span>
<span data-ttu-id="b2e0b-116">後でインポートに使用できるエンティティ テンプレート ファイルを生成するためにエクスポート機能を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-116">It is a common practice to use the export functionality to generate the entity template file which can be later used for imports.</span></span> <span data-ttu-id="b2e0b-117">ただし、"最初の行ヘッダー" が "いいえ" になっている固定長形式でテンプレートをエクスポートしますが (設定されたソース データ形式で)、エクスポートしたテンプレートには列の名前がありません。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-117">However, while exporting the template, in fixed width format with 'First row header' set to 'No' (in source data formats set up), the exported template will not have the column names.</span></span> <span data-ttu-id="b2e0b-118">このファイルのインポート時、このエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-118">When this file is imported, it will result in this error.</span></span> 

## <a name="data-package-download---error-downloading-data-package-for-job--record-for-id---guid-not-found"></a><span data-ttu-id="b2e0b-119">データ パッケージ ダウンロード - ジョブ '' のデータ パッケージのダウンロード エラーです。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-119">Data package download - Error downloading data package for job ''.</span></span> <span data-ttu-id="b2e0b-120">ID - {GUID} のレコードが見つかりません</span><span class="sxs-lookup"><span data-stu-id="b2e0b-120">Record for ID - {GUID} not found</span></span>
<span data-ttu-id="b2e0b-121">これが発生するシナリオは、開発環境などの環境が UAT などの別の環境にあるデータベースをポイントしており、エクスポート ジョブがソース環境から実行される場合などがあります。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-121">One of the scenarios where this can happen is when the environment, such as the dev environment, points to the database in another environment, such as UAT, and the export job is run from the source environment.</span></span> <span data-ttu-id="b2e0b-122">この例では、開発です。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-122">which is dev in this example.</span></span> <span data-ttu-id="b2e0b-123">エクスポートしたファイルは、ソース環境 (この例では開発) に関連付けられている blob ストレージにアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-123">The exported file gets uploaded to the blob storage that is associated with the source environment (dev, in this example).</span></span> <span data-ttu-id="b2e0b-124">ただし、データベースが共有されているため、このジョブはターゲット環境 (UAT) にも表れます。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-124">However, this job will also show up in the target environment (UAT) since the database is shared.</span></span> <span data-ttu-id="b2e0b-125">**ファイルをダウンロード**オプションを使用してエクスポートしたファイルをダウンロードしようとする場合、ダウンロード元となるターゲット環境 (UAT) の blob ストレージにファイルが存在しないために、このエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2e0b-125">If a you try to download the exported file using the **Download file** option, this error will display because the file does not exist in the blob storage of the target environment (UAT) from where you are trying to download.</span></span>
 


---
title: ファイルのアップロード コントロール
description: このトピックでは、ファイル アップロード コントロールについて説明します。 このコントロールを使用して、ファイルをアップロードできます。
author: aneesmsft
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 54311
ms.assetid: 82f47d4d-912c-4f85-81f9-b09c723f72fc
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30de4a3b6b5206114bb500648bce82011cccbf55
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686598"
---
# <a name="file-upload-control"></a><span data-ttu-id="9ec71-104">ファイルのアップロード コントロール</span><span class="sxs-lookup"><span data-stu-id="9ec71-104">File upload control</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="9ec71-105">このトピックでは、ファイル アップロード コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-105">This topic provides information about the file upload control.</span></span> <span data-ttu-id="9ec71-106">このコントロールを使用して、ファイルをアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-106">This control lets users upload files.</span></span>

<a name="overview"></a><span data-ttu-id="9ec71-107">概要</span><span class="sxs-lookup"><span data-stu-id="9ec71-107">Overview</span></span>
--------

<span data-ttu-id="9ec71-108">ファイル アップロード コントロールを使用してユーザーはファイルをアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-108">The file upload control lets users upload a file.</span></span> <span data-ttu-id="9ec71-109">また、これにより開発者は要件に基づいてアップロード処理を制御し、アップロードされたファイルを管理します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-109">It also lets developers control the upload process and manage the file that is uploaded, based on their requirements.</span></span> 

<span data-ttu-id="9ec71-110">[![ファイル アップロード コントロールの図](./media/fileupload001.png)](./media/fileupload001.png)</span><span class="sxs-lookup"><span data-stu-id="9ec71-110">[![Illustration of file upload control](./media/fileupload001.png)](./media/fileupload001.png)</span></span> 

<span data-ttu-id="9ec71-111">ファイル アップロード コントロールには 3 つのスタイルがあります。</span><span class="sxs-lookup"><span data-stu-id="9ec71-111">The file upload control can have three styles.</span></span> <span data-ttu-id="9ec71-112">スタイルを制御するには、**スタイル** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-112">You control the style by using the **Style** property.</span></span>

-   <span data-ttu-id="9ec71-113">**標準** スタイルは、**参照**、**アップロード**、および **キャンセル** ボタンと同時にファイル名フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-113">The **Standard** style shows the file name field together with **Browse**, **Upload**, and **Cancel** buttons.</span></span>
-   <span data-ttu-id="9ec71-114">**最小限** スタイルは **参照** ボタンのみ表示します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-114">The **Minimal** style shows only the **Browse** button.</span></span>
-   <span data-ttu-id="9ec71-115">**MinimalWithFileName** スタイルは、ファイル名フィールドと **参照** ボタンを表示します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-115">The **MinimalWithFileName** style shows the file name field and the **Browse** button.</span></span>

<span data-ttu-id="9ec71-116">ファイル アップロード コントロールの **FileTypesAccepted** プロパティを使用すると、ユーザーがアップロードできるファイルの種類を制限できます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-116">The **FileTypesAccepted** property of the file upload control lets you limit the types of files that users can upload.</span></span> <span data-ttu-id="9ec71-117">ユーザーがアップロードできるファイル タイプは、主に関連するアップロード方法によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-117">The file types that users can upload are primarily controlled by the associated upload strategy.</span></span> <span data-ttu-id="9ec71-118">ファイル アップロード コントロールの **FileTypesAccepted** プロパティは、さらに制限が必要な場合にのみ使用してください。</span><span class="sxs-lookup"><span data-stu-id="9ec71-118">The **FileTypesAccepted** property on the file upload control should be used only if further restrictions are required.</span></span> <span data-ttu-id="9ec71-119">アップロード コントロールは、アップロード戦略によって制限されているファイルの種類を指定するしようとすると、**参照** ボタンが使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="9ec71-119">If the upload control tries to specify file types that are restricted by the upload strategy, the **Browse** button becomes unavailable.</span></span>

| <span data-ttu-id="9ec71-120">許可されたファイル タイプ</span><span class="sxs-lookup"><span data-stu-id="9ec71-120">Allowed file types</span></span>    | <span data-ttu-id="9ec71-121">アップロード戦略の許可されたファイル タイプ</span><span class="sxs-lookup"><span data-stu-id="9ec71-121">Allowed file types from the upload strategy</span></span> | <span data-ttu-id="9ec71-122">最終結果</span><span class="sxs-lookup"><span data-stu-id="9ec71-122">Final result</span></span>                          |
|-----------------------|---------------------------------------------|---------------------------------------|
| <span data-ttu-id="9ec71-123">「.jpg、.png」</span><span class="sxs-lookup"><span data-stu-id="9ec71-123">".jpg,.png"</span></span>           | <span data-ttu-id="9ec71-124">「.jpg、.png、.gif、.txt」</span><span class="sxs-lookup"><span data-stu-id="9ec71-124">".jpg,.png,.gif,.txt"</span></span>                       | <span data-ttu-id="9ec71-125">「.jpg、.png」</span><span class="sxs-lookup"><span data-stu-id="9ec71-125">".jpg,.png"</span></span>                           |
| <span data-ttu-id="9ec71-126">「image/png」</span><span class="sxs-lookup"><span data-stu-id="9ec71-126">"image/png"</span></span>           | <span data-ttu-id="9ec71-127">「image/\*」</span><span class="sxs-lookup"><span data-stu-id="9ec71-127">"image/\*"</span></span>                                  | <span data-ttu-id="9ec71-128">「image/png」</span><span class="sxs-lookup"><span data-stu-id="9ec71-128">"image/png"</span></span>                           |
| <span data-ttu-id="9ec71-129">「image/\*」</span><span class="sxs-lookup"><span data-stu-id="9ec71-129">"image/\*"</span></span>            | <span data-ttu-id="9ec71-130">「image/png」</span><span class="sxs-lookup"><span data-stu-id="9ec71-130">"image/png"</span></span>                                 | <span data-ttu-id="9ec71-131">**参照** ボタンは使用できません。</span><span class="sxs-lookup"><span data-stu-id="9ec71-131">The **Browse** button is unavailable.</span></span> |
| <span data-ttu-id="9ec71-132">「.jpg、.png、.gif、.txt」</span><span class="sxs-lookup"><span data-stu-id="9ec71-132">".jpg,.png,.gif,.txt"</span></span> | <span data-ttu-id="9ec71-133">「.jpg、.png」</span><span class="sxs-lookup"><span data-stu-id="9ec71-133">".jpg,.png"</span></span>                                 | <span data-ttu-id="9ec71-134">**参照** ボタンは使用できません。</span><span class="sxs-lookup"><span data-stu-id="9ec71-134">The **Browse** button is unavailable.</span></span> |

<span data-ttu-id="9ec71-135">**OnBrowseButtonClicked**、**OnUploadAttemptStarted**、および **OnUploadCompleted** オーバーライドを使用すると、ファイル アップロード プロセスの様々なステージにフックすることができます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-135">You can use the **OnBrowseButtonClicked**, **OnUploadAttemptStarted**, and **OnUploadCompleted** overrides to hook into the various stages of the file upload process.</span></span> <span data-ttu-id="9ec71-136">また、カスタム ファイル アップロード戦略を作成して、**FileUpload Strategy Class** プロパティを使用してファイル アップロード コントロールと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-136">You can also create custom file upload strategies and associate them with a file upload control by using the **FileUpload Strategy Class** property.</span></span>

## <a name="design-classes"></a><span data-ttu-id="9ec71-137">デザイン クラス</span><span class="sxs-lookup"><span data-stu-id="9ec71-137">Design classes</span></span>
<span data-ttu-id="9ec71-138">開発者がファイル アップロード コントロールのために使用できる基底クラスは 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="9ec71-138">There are two base classes that developers can work with for the file upload control:</span></span>

-   <span data-ttu-id="9ec71-139">**戦略クラスをアップロード** – この基底クラスにより、開発者はユーザーがアップロードできるファイルの種類およびファイルの最大サイズなどのアップロードされたファイルに適用される必要があるさまざまなパラメータを制御できます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-139">**Upload strategy class** – This base class lets developers control various parameters that should be enforced for uploaded files, such as the types of files that a user can upload and the maximum size of a file.</span></span> <span data-ttu-id="9ec71-140">また、これにより開発者はアップロード済みのファイルが保存される場所および方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-140">It also lets developers determine where and how the uploaded file should be stored.</span></span> <span data-ttu-id="9ec71-141">アップロード戦略に使用されるすべての派生クラスは、抽象 **FileUploadStrategyBase** クラスから継承する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ec71-141">All derived classes used for upload strategies must inherit from the abstract **FileUploadStrategyBase** class.</span></span>
-   <span data-ttu-id="9ec71-142">**結果クラスをアップロード** – この基底クラスにより、開発者は、名前、コンテンツ タイプ、アップロード状態など、ユーザーがアップロードしたファイルの詳細にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-142">**Upload result class** – This base class lets developers access the details of a file that was uploaded by a user, such as its name, content type, and upload status.</span></span> <span data-ttu-id="9ec71-143">また、これにより開発者は対応するファイルを開いたり削除したりします。</span><span class="sxs-lookup"><span data-stu-id="9ec71-143">It also lets developers open and delete the corresponding file.</span></span> <span data-ttu-id="9ec71-144">アップロード結果の特殊化に使用されるすべての派生クラスは、抽象 **FileUploadResultBase** クラスから継承する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ec71-144">All derived classes used for specializing upload results must inherit from the abstract **FileUploadResultBase** class.</span></span>

<span data-ttu-id="9ec71-145">このフレームワークは、**FileUploadTemporaryStorageStrategy** という名前のデフォルトのアップロード戦略クラスと **FileUploadTemporaryStorageResult** というデフォルトのアップロード結果クラスを提供します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-145">The framework provides a default upload strategy class that is named **FileUploadTemporaryStorageStrategy** and a default upload result class that is named **FileUploadTemporaryStorageResult**.</span></span> <span data-ttu-id="9ec71-146">このアップロード結果クラスは、アップロードされたファイルを一時的な BLOB ストレージに格納し、ダウンロード URL を提供します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-146">This upload result class stores uploaded files to the temporary blob storage and provides a download URL.</span></span> <span data-ttu-id="9ec71-147">開発者は、独自のカスタム アップロード戦略を実装し、必要に応じて結果クラスをアップロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-147">Developers can also implement their own custom upload strategy and upload result classes as required.</span></span> <span data-ttu-id="9ec71-148">アップロード方法については、**FileUploadStrategyBase** クラスからの 2 つの抽象メソッドは、実装される必要があります: **uploadFile** および **getResultClassName**。</span><span class="sxs-lookup"><span data-stu-id="9ec71-148">For the upload strategy, two abstract methods from the **FileUploadStrategyBase** class must be implemented: **uploadFile** and **getResultClassName**.</span></span> <span data-ttu-id="9ec71-149">**uploadFile** メソッドは、ファイルが保管される場所および方法を処理します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-149">The **uploadFile** method handles where and how the file is stored.</span></span> <span data-ttu-id="9ec71-150">**getResultClassName** メソッドは、この方法で使用されるアップロード結果クラスを取得します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-150">The **getResultClassName** method retrieves the upload result class that is used in this strategy.</span></span> <span data-ttu-id="9ec71-151">**FileUploadResultBase** クラスには、ファイル名、アップロード ステータス、ファイルのコンテンツタイプ、およびログ メッセージのフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="9ec71-151">The **FileUploadResultBase** class has fields for the file name, the upload status, the content type of the file, and the log message.</span></span> <span data-ttu-id="9ec71-152">このクラスは、必要に応じて拡張できます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-152">This class can be extended as required.</span></span> <span data-ttu-id="9ec71-153">すべての新しいプロパティはシリアル化および逆シリアル化することができます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-153">All new properties should be able to be serialized and deserialized.</span></span> <span data-ttu-id="9ec71-154">**openResult** メソッドはストリームとしてファイルを開き、**deleteResult** メソッドは対応するデータ ストレージからファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-154">The **openResult** method opens the file as a stream, and the **deleteResult** method deletes the file from the corresponding data storage.</span></span>

## <a name="sequence-diagram"></a><span data-ttu-id="9ec71-155">シーケンス図</span><span class="sxs-lookup"><span data-stu-id="9ec71-155">Sequence diagram</span></span>
<span data-ttu-id="9ec71-156">ファイル アップロード コントロールは、クライアントのファイルとアップロード方法を受け入れ、ファイル サービスに送信します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-156">The file upload control accepts the file and upload strategy in the client, and sends them to the file services.</span></span> <span data-ttu-id="9ec71-157">ファイル サービスは新しいセッションを開始し、戦略クラスのインスタンスを作成し、**uploadFile** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-157">The file services start a new session, create an instance of a strategy class, and call the **uploadFile** method.</span></span> <span data-ttu-id="9ec71-158">**uploadFile** メソッドがデータ ソース内へのファイルの格納を完了したとき、ファイルのアップロード結果クラスがファイル サービスへを返されます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-158">When the **uploadFile** method has finished storing the file in the data source, a file upload result class returns to the file services.</span></span> <span data-ttu-id="9ec71-159">このクラスはクライアントに送り返され、後処理に対処する **OnUploadCompleted** イベントをトリガーする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9ec71-159">This class is sent back to the client, which might trigger the **OnUploadCompleted** event to deal with the post-process.</span></span> 

<span data-ttu-id="9ec71-160">[![ファイル アップロード シーケンス ダイアグラム](./media/fileuploadcontrolusageanddesign1.png)](./media/fileuploadcontrolusageanddesign1.png)</span><span class="sxs-lookup"><span data-stu-id="9ec71-160">[![File upload sequence diagram](./media/fileuploadcontrolusageanddesign1.png)](./media/fileuploadcontrolusageanddesign1.png)</span></span>

## <a name="scanning-uploaded-files-for-viruses-and-malicious-code"></a><span data-ttu-id="9ec71-161">アップロードされたファイルでのウイルスおよび悪意のあるコードのスキャン</span><span class="sxs-lookup"><span data-stu-id="9ec71-161">Scanning uploaded files for viruses and malicious code</span></span>
<span data-ttu-id="9ec71-162">ファイルをシステムにアップロードする前に、ウイルスや悪質なコードをスキャンすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9ec71-162">Before you upload a file into the system, you might want to scan it for viruses or malicious code.</span></span> <span data-ttu-id="9ec71-163">したがって、バージョン10.0.12 以降では、ユーザーが選択したファイル スキャン ソフトウェアをファイル アップロード プロセスに統合できるように、拡張ポイントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-163">Therefore, in version 10.0.12 and later, an extension point is available so that customers can integrate the file scanning software of their choice into the file upload process.</span></span> <span data-ttu-id="9ec71-164">添付ファイルのスキャンにも、同様の拡張ポイントが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="9ec71-164">Similar extension points are also available for scanning attachments.</span></span> <span data-ttu-id="9ec71-165">これらの拡張ポイントの詳細については、[ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ec71-165">For more information about those extension points, see [Configure document management](../../fin-ops/organization-administration/configure-document-management.md).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="9ec71-166">初期状態では、Finance and Operations アプリはファイルのウイルスや悪意のあるコードをスキャンせず、ファイルをスキャンするための特定のソフトウェアはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="9ec71-166">Out of the box, Finance and Operations apps don't scan files for viruses and malicious code, and we don't recommend specific software for file scanning.</span></span> <span data-ttu-id="9ec71-167">代わりに、お客様は、独自のファイル スキャン ソフトウェアを選択し、ファイルのスキャンにソフトウェアまたはサービスを使用できるように適切なコードをデリゲート ハンドラーに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ec71-167">Instead, customers are responsible for choosing their own file scanning software, and for adding the appropriate code to the delegate handlers so that they can use the software or service of their choice to scan files.</span></span>

<span data-ttu-id="9ec71-168">特に、**FileUploadResultBase** クラスは **delegateScanStream()** デリゲートを公開します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-168">In particular, the **FileUploadResultBase** class exposes the **delegateScanStream()** delegate.</span></span> <span data-ttu-id="9ec71-169">このデリゲートは、**アップロード戦略クラス** が特殊化されているファイル アップロード シナリオに適用されます。</span><span class="sxs-lookup"><span data-stu-id="9ec71-169">This delegate applies to any file upload scenario where the **Upload strategy class** has been specialized.</span></span> <span data-ttu-id="9ec71-170">スキャン サービスによってファイルが悪質であると判断された場合、アップロード プロセスは失敗します。</span><span class="sxs-lookup"><span data-stu-id="9ec71-170">The upload process will fail if the scanning service determines that the file is malicious.</span></span>    

### <a name="implementation-details"></a><span data-ttu-id="9ec71-171">実装詳細</span><span class="sxs-lookup"><span data-stu-id="9ec71-171">Implementation details</span></span>
<span data-ttu-id="9ec71-172">次の **ScanDocuments** クラスの例は、ハンドラーの定型コードを示しています。</span><span class="sxs-lookup"><span data-stu-id="9ec71-172">The following example of the **ScanDocuments** class shows boilerplate code for the handler.</span></span> <span data-ttu-id="9ec71-173">デリゲートのハンドラーを実装する方法の一般情報については、[要求または応答シナリオの EventHandlerResult クラス](../dev-tools/event-handler-result-class.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ec71-173">For general information about how to implement handlers for delegates, see [EventHandlerResult classes in request or response scenarios](../dev-tools/event-handler-result-class.md).</span></span>

```xpp
    public final class ScanDocuments
    {

        [SubscribesTo(classStr(FileUploadResultBase), staticDelegateStr(FileUploadResultBase, delegateScanStream))]
        public static void FileUploadResultBase_delegateScanStream(System.IO.Stream _stream, EventHandlerRejectResult _validationResult)
        {
            if (!ScanDocuments::scanStream(_stream))
            {
                _validationResult.reject();           
            }
        }

        private static boolean scanStream(System.IO.Stream _stream)
        {
            /* 
            Custom implementation required for connecting to a scanning service
            If document scanning process found an issue, return false; otherwise, return true;
            */
            return true;
        }
    }
```


---
title: 生成されたドキュメント用にカスタマイズされた保存先を指定します
description: このトピックでは、電子申告 (ER) 形式が生成するドキュメントの保存先のリストを拡張する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 3ea9de81045dfd01ffec2c8a1d98ea2ba4f2c49a
ms.sourcegitcommit: 0e01d3907b70261aee2df3e3ce0dde2f1343a43a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/27/2019
ms.locfileid: "770091"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="33589-103">生成されたドキュメント用にカスタマイズされた保存先を指定します</span><span class="sxs-lookup"><span data-stu-id="33589-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="33589-104">電子申告 (ER) フレームワークのアプリケーション プログラミング インターフェイス (API) により、電子申告 (ER) 形式が生成するドキュメントの保存先のリストを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="33589-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="33589-105">このトピックには、カスタマイズされた保存先を追加するために完了する必要のある主要なタスクに関する概要が含まれます。</span><span class="sxs-lookup"><span data-stu-id="33589-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="33589-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="33589-106">Prerequisites</span></span>

<span data-ttu-id="33589-107">継続的ビルドをサポートする Microsoft Dynamics 365 for Finance and Operations トポロジを配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33589-107">You must deploy a Microsoft Dynamics 365 for Finance and Operations topology that supports continuous build.</span></span> <span data-ttu-id="33589-108">(詳細については、[継続的ビルドとテストの自動化をサポートするトポロジの配置](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation) を参照してください。) 次のロールの 1 つに対して Finance and Operations トポロジにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="33589-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this Finance and Operations topology for one of the following roles:</span></span>

- <span data-ttu-id="33589-109">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="33589-109">Electronic reporting developer</span></span>
- <span data-ttu-id="33589-110">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="33589-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="33589-111">システム管理者</span><span class="sxs-lookup"><span data-stu-id="33589-111">System administrator</span></span>

<span data-ttu-id="33589-112">この Finance and Operations トポロジの開発環境にもアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="33589-112">You must also have access to the development environment for this Finance and Operations topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="33589-113">ER フォーマット構成の作成またはインポート</span><span class="sxs-lookup"><span data-stu-id="33589-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="33589-114">現在の Finance and Operations トポロジでは、[新しい ER フォーマットを作成して](tasks/er-format-configuration-2016-11.md)、カスタマイズされた保存先を追加するドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="33589-114">In the current Finance and Operations topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="33589-115">または、[既存の ER フォーマットをこのトポロジにインポートします](general-electronic-reporting-manage-configuration-lifecycle.md)。</span><span class="sxs-lookup"><span data-stu-id="33589-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![形式デザイナーのページ](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="33589-117">作成またはインポートする ER フォーマットには、次のフォーマット エレメントのうち少なくとも 1 つを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="33589-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="33589-118">ファイル</span><span class="sxs-lookup"><span data-stu-id="33589-118">File</span></span>
> - <span data-ttu-id="33589-119">フォルダー</span><span class="sxs-lookup"><span data-stu-id="33589-119">Folder</span></span>
> - <span data-ttu-id="33589-120">マージ</span><span class="sxs-lookup"><span data-stu-id="33589-120">Merger</span></span>
> - <span data-ttu-id="33589-121">添付ファイル</span><span class="sxs-lookup"><span data-stu-id="33589-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="33589-122">新しいドキュメント タイプの作成</span><span class="sxs-lookup"><span data-stu-id="33589-122">Create a new document type</span></span>

<span data-ttu-id="33589-123">ER フォーマットが生成するドキュメントのルーティング方法を指定するには、[ER の送信先](electronic-reporting-destinations.md) を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33589-123">To specify how documents that an ER format generates are routed, you must configure [ER destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="33589-124">生成するドキュメントをファイルとして保存するように構成する各 ER の送信先では、ドキュメントのドキュメント タイプを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33589-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="33589-125">異なる ER フォーマットが生成するドキュメントをルーティングするには、異なるドキュメント タイプが使用できます。</span><span class="sxs-lookup"><span data-stu-id="33589-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="33589-126">前に作成またはインポートした ER フォーマット用に、新しい [ドキュメント タイプ](../../fin-and-ops/organization-administration/configure-document-management.md) を追加します。</span><span class="sxs-lookup"><span data-stu-id="33589-126">Add a new [document type](../../fin-and-ops/organization-administration/configure-document-management.md) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="33589-127">次の図では、ドキュメント タイプは **FileX** です。</span><span class="sxs-lookup"><span data-stu-id="33589-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="33589-128">このドキュメント タイプをその他のドキュメント タイプから区別するには、名前に特定のキーワードを含めます。</span><span class="sxs-lookup"><span data-stu-id="33589-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="33589-129">たとえば、次の図では、名前は **(ローカル) フォルダー**です。</span><span class="sxs-lookup"><span data-stu-id="33589-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="33589-130">**クラス** フィールドには、**ファイルの添付**を指定します。</span><span class="sxs-lookup"><span data-stu-id="33589-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="33589-131">**グループ** フィールドには、**ファイル**を指定します。</span><span class="sxs-lookup"><span data-stu-id="33589-131">In the **Group** field, specify **File**.</span></span>

![ドキュメント タイプ ページ](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="33589-133">ドキュメント タイプは会社固有のものです。</span><span class="sxs-lookup"><span data-stu-id="33589-133">Document types are company-specific.</span></span> <span data-ttu-id="33589-134">複数の会社で構成されている送信先と ER フォーマットを使用するには、各会社ごとに個別のドキュメント タイプを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33589-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="33589-135">ソース コードの確認</span><span class="sxs-lookup"><span data-stu-id="33589-135">Review source code</span></span>

<span data-ttu-id="33589-136">**ERDocuManagement** クラスの **insertFile()** メソッドのコードを確認します。</span><span class="sxs-lookup"><span data-stu-id="33589-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="33589-137">生成されたファイルがレコードに関連付けられた時、**AttachingFile()** イベントが発生することに注意します。</span><span class="sxs-lookup"><span data-stu-id="33589-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

```
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="33589-138">**AttachingFile()** イベントは、次の ER の送信先が処理される時に発生します。</span><span class="sxs-lookup"><span data-stu-id="33589-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="33589-139">**アーカイブ** – この送信先が使用される場合、実行される ER フォーマット用の新しいレコードが ERFormatMappingRunJobTable テーブルに作成されます。</span><span class="sxs-lookup"><span data-stu-id="33589-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="33589-140">このレコードの **Archived** フィールドが、**False** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="33589-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="33589-141">ER フォーマットが正常に実行されると、生成されるドキュメントがこのレコードに関連付けられ、**AttachingFile()** イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="33589-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="33589-142">この ER 送信先で選択したドキュメント タイプにより、添付ファイルの保存先が決定されます (Microsoft Azure ストレージまたは Microsoft SharePoint フォルダー)。</span><span class="sxs-lookup"><span data-stu-id="33589-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="33589-143">**ジョブ アーカイブ** – この送信先が使用される場合、実行される ER フォーム用の新しいレコードが ERFormatMappingRunJobTable テーブルに作成されます。</span><span class="sxs-lookup"><span data-stu-id="33589-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="33589-144">このレコードの **Archived** フィールドが、**True** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="33589-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="33589-145">ER フォーマットが正常に実行されると、生成されるドキュメントがこのレコードに関連付けられ、**AttachingFile()** イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="33589-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="33589-146">ER パラメーターで構成されるドキュメント タイプにより、添付ファイルの保存先が決定されます (Azure ストレージまたは SharePoint フォルダー)。</span><span class="sxs-lookup"><span data-stu-id="33589-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![電子申告のパラメーター ページ](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="33589-148">ER 送信先の構成</span><span class="sxs-lookup"><span data-stu-id="33589-148">Configure an ER destination</span></span>

1. <span data-ttu-id="33589-149">作成またはインポートした ER フォーマットについて、前述の要素 (ファイル、フォルダー、マージ、または添付ファイル) の 1 つに対してアーカイブされた送信先を構成します。</span><span class="sxs-lookup"><span data-stu-id="33589-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="33589-150">ガイダンスについては、[ER コンフィギュレーション先](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33589-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="33589-151">構成された送信先用にすでに追加したドキュメント タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="33589-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="33589-152">(このトピックの例では、ドキュメント タイプは **FileX** です。)</span><span class="sxs-lookup"><span data-stu-id="33589-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![送信先設定ダイアログ ボックス](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="33589-154">ソース コードの修正</span><span class="sxs-lookup"><span data-stu-id="33589-154">Modify source code</span></span>

1. <span data-ttu-id="33589-155">Microsoft Visual Studio プロジェクトに新しいクラスを追加し、前述した **AttachingFile()** イベントをサブスクライブするためのコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="33589-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="33589-156">(使用される拡張性パターンの詳細については、[EventHandlerResult を使用した応答](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result) を参照してください。) たとえば、新しいクラスで、次のアクションを実行するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="33589-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="33589-157">Application Object Server (AOS) サービスを実行するサーバーのローカル ファイル システムのフォルダに、生成したファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="33589-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="33589-158">新しいドキュメント タイプ (たとえば、名前に "(ローカル)" キーワードが含まれている **FileX** タイプ) が ER 実行ジョブ ログのレコードにファイルが関連付けられている時に使用される場合にのみ、これら生成されたファイルは保存されます。</span><span class="sxs-lookup"><span data-stu-id="33589-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="33589-159">プロジェクトのリビルドします。</span><span class="sxs-lookup"><span data-stu-id="33589-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="33589-160">作成またはインポートした ER フォーマットの実行</span><span class="sxs-lookup"><span data-stu-id="33589-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="33589-161">作成またはインポートした ER フォーマットを実行します。</span><span class="sxs-lookup"><span data-stu-id="33589-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="33589-162">**組織管理 \> 電子申告 \> 電子申告ジョブ**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="33589-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="33589-163">この実行ジョブのために作成され、関連付けられた生成ファイルを持つレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="33589-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="33589-164">ローカルの **C:\\0** フォルダーを表示し、同じ生成ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="33589-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33589-165">追加リソース</span><span class="sxs-lookup"><span data-stu-id="33589-165">Additional resources</span></span>

- [<span data-ttu-id="33589-166">電子申告の送信先</span><span class="sxs-lookup"><span data-stu-id="33589-166">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="33589-167">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="33589-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)

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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5e9afad936a353c8db3c316ad45c4ce28d33b129
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680809"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>生成されたドキュメント用にカスタマイズされた保存先を指定します

[!include[banner](../includes/banner.md)]

電子申告 (ER) フレームワークのアプリケーション プログラミング インターフェイス (API) により、電子申告 (ER) 形式が生成するドキュメントの保存先のリストを拡張することができます。 このトピックには、カスタマイズされた保存先を追加するために完了する必要のある主要なタスクに関する概要が含まれます。

## <a name="prerequisites"></a>必要条件

継続的ビルドをサポートするトポロジを配置する必要があります。 (詳細については、[継続的ビルドとテストの自動化をサポートするトポロジの配置](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation) を参照してください。) 次のロールの 1 つに対してこのトポロジにアクセスできる必要があります。

- 電子申告開発者
- 電子申告機能コンサルタント
- システム管理者

また、このトポロジの開発環境にもアクセスできる必要があります。

## <a name="create-or-import-an-er-format-configuration"></a>ER フォーマット構成の作成またはインポート

現在のトポロジでは、[新しい ER フォーマットを作成して](tasks/er-format-configuration-2016-11.md)、カスタマイズされた保存先を追加したいドキュメントを生成します。 または、[既存の ER フォーマットをこのトポロジにインポートします](general-electronic-reporting-manage-configuration-lifecycle.md)。

![形式デザイナーのページ](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> 作成またはインポートする ER フォーマットには、次のフォーマット エレメントのうち少なくとも 1 つを含める必要があります。
>
> - ファイル
> - フォルダー
> - マージ
> - 添付ファイル

## <a name="create-a-new-document-type"></a>新しいドキュメント タイプの作成

ER フォーマットが生成するドキュメントのルーティング方法を指定するには、[電子申告 (ER) の送信先](electronic-reporting-destinations.md) を構成する必要があります。 生成するドキュメントをファイルとして保存するように構成する各 ER の送信先では、ドキュメントのドキュメント タイプを指定する必要があります。 異なる ER フォーマットが生成するドキュメントをルーティングするには、異なるドキュメント タイプが使用できます。

1. 前に作成またはインポートした ER フォーマット用に、新しい [ドキュメント タイプ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) を追加します。 次の図では、ドキュメント タイプは **FileX** です。
2. このドキュメント タイプをその他のドキュメント タイプから区別するには、名前に特定のキーワードを含めます。 たとえば、次の図では、名前は **(ローカル) フォルダー** です。
3. **クラス** フィールドには、**ファイルの添付** を指定します。
4. **グループ** フィールドには、**ファイル** を指定します。

![ドキュメント タイプ ページ](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> ドキュメント タイプは会社固有のものです。 複数の会社で構成されている送信先と ER フォーマットを使用するには、各会社ごとに個別のドキュメント タイプを構成する必要があります。

## <a name="review-source-code"></a>ソース コードの確認

**ERDocuManagement** クラスの **insertFile()** メソッドのコードを確認します。 生成されたファイルがレコードに関連付けられた時、**AttachingFile()** イベントが発生することに注意します。


```xpp
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

**AttachingFile()** イベントは、次の ER の送信先が処理される時に発生します。

- **アーカイブ** – この送信先が使用される場合、実行される ER フォーマット用の新しいレコードが ERFormatMappingRunJobTable テーブルに作成されます。 このレコードの **Archived** フィールドが、**False** に設定されます。 ER フォーマットが正常に実行されると、生成されるドキュメントがこのレコードに関連付けられ、**AttachingFile()** イベントが発生します。 この ER 送信先で選択したドキュメント タイプにより、添付ファイルの保存先が決定されます (Microsoft Azure ストレージまたは Microsoft SharePoint フォルダー)。
- **ジョブ アーカイブ** – この送信先が使用される場合、実行される ER フォーム用の新しいレコードが ERFormatMappingRunJobTable テーブルに作成されます。 このレコードの **Archived** フィールドが、**True** に設定されます。 ER フォーマットが正常に実行されると、生成されるドキュメントがこのレコードに関連付けられ、**AttachingFile()** イベントが発生します。 ER パラメーターで構成されるドキュメント タイプにより、添付ファイルの保存先が決定されます (Azure ストレージまたは SharePoint フォルダー)。

![電子申告のパラメーター ページ](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>ER 送信先の構成

1. 作成またはインポートした ER フォーマットについて、前述の要素 (ファイル、フォルダー、マージ、または添付ファイル) の 1 つに対してアーカイブされた送信先を構成します。 ガイダンスについては、[ER コンフィギュレーション先](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11) を参照してください。
2. 構成された送信先用にすでに追加したドキュメント タイプを使用します。 (このトピックの例では、ドキュメント タイプは **FileX** です。)

![送信先設定ダイアログ ボックス](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>ソース コードの修正

1. Microsoft Visual Studio プロジェクトに新しいクラスを追加し、前述した **AttachingFile()** イベントをサブスクライブするためのコードを記述します。 (使用される拡張性パターンの詳細については、[EventHandlerResult を使用した応答](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result) を参照してください。) たとえば、新しいクラスで、次のアクションを実行するコードを記述します。

    1. Application Object Server (AOS) サービスを実行するサーバーのローカル ファイル システムのフォルダに、生成したファイルを保存します。
    2. 新しいドキュメント タイプ (たとえば、名前に "(ローカル)" キーワードが含まれている **FileX** タイプ) が ER 実行ジョブ ログのレコードにファイルが関連付けられている時に使用される場合にのみ、これら生成されたファイルは保存されます。

    ```xpp
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

2. プロジェクトのリビルドします。

## <a name="run-the-er-format-that-you-created-or-imported"></a>作成またはインポートした ER フォーマットの実行

1. 作成またはインポートした ER フォーマットを実行します。
2. **組織管理 \> 電子申告 \> 電子申告ジョブ** の順に選択します。 この実行ジョブのために作成され、関連付けられた生成ファイルを持つレコードを検索します。
3. ローカルの **C:\\0** フォルダーを表示し、同じ生成ファイルを検索します。

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)
- [拡張機能のホーム ページ](../extensibility/extensibility-home-page.md)

---
title: 画像のアップロード
description: この記事では、Microsoft Dynamics 365 Commerce サイト ビルダーの画像アップロードの方法について説明します。
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d937e8c0e00ce28b0e4a4c2feab3ac1c8f075916
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283382"
---
# <a name="upload-images"></a>画像のアップロード

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce サイト ビルダーの画像アップロードの方法について説明します。

コマース サイト ビルダーのメディア ライブラリーを使用すると、フォルダーを使用してイメージを単独または一括でアップロードできます。 イメージの変更コンポーネントを使用すると、さまざまなビューポートとそのブレークポイントに対する画像が自動的に最適化されるので、最大解像度と品質で画像のバージョンをアップロードする必要があります。

### <a name="image-information-specified-during-upload"></a>アップロード中に指定された画像情報

画像をアップロードする場合は、次の情報を指定できます。

- **タイトル、代替テキスト、説明、キーワード**: イメージのメタデータまたは画像。 タイトルと代替テキストは必要な値です。
- **カテゴリの選択**:
    - **なし**: E コマースのストーリーテリング イメージまたは画像に使用されます。
    - **製品、カテゴリ、顧客、従業員、カタログ**: Dynamics 365 Commerce オムニ チャネルのイメージまたは画像に使用されます。
- **アップロード後にアセットを公開**: このチェック ボックスがオンになっている場合は、アップロード後すぐにイメージまたは画像が公開されます。

> [!NOTE]
> - カテゴリが割り当てられた画像の資産には、特定のカテゴリの資産の検索を支援するキーワードとして自動的にカテゴリにタグが付けられます。
> - 製品の詳細ページでは、製品名を使用して **Alt テキスト** が動的に生成されます。したがって、製品画像の **Alt テキスト** を変更すると、表示される画像には影響はありません。

### <a name="naming-conventions-for-omni-channel-images"></a>オムニ チャネル画像の命名規則 

メディア ライブラリをオムニ チャネル画像のバックエンドとしてコンフィギュレーションしている場合は、イメージ カテゴリを使用して、アップロードしたイメージが属するカテゴリを指定できます。 また、販売時点管理 (POS)などのその他のチャネルによって、画像が正しく取得されているか確認するために命名規則も用意されています。

既定の命名規則は、カテゴリによって異なります。
- カタログの画像は、"**/カタログ/\{LanguageId\}/\{CatalogName\}.jpg**" という名前にする必要があります
- カテゴリ画像は、"**/カテゴリ/\{CategoryName\}.png**" という名前にする必要があります
- 顧客の画像は、"**/顧客/\{CustomerNumber\}.jpg**" という名前にする必要があります
- 従業員の画像は、"**/作業者/\{WorkerNumber\}.jpg**" という名前にする必要があります
- 製品画像は、"**/製品/\{ProductNumber\}\_000_001.png**" という名前にする必要があります
    - 001 は画像の順序で、001、002、003、004、または 005 とすることができます
- 製品バリアントの画像は、"**/製品/\{ProductNumber\} \^ \{スタイル\} \^ \{サイズ\} \^ \{色\} \^\_000_001.png**" という名前にする必要があります
    - 例: 93039 \^ &nbsp;\^ 2 \^ 黒 \^\_000_001.png
- コンフィギュレーション分析コードの製品バリアント画像は、"**/製品/\{ProductNumber\} \^ \{コンフィギュレーション\}\_000_001.png**" という名前にする必要があります
    - 例: 93039\^ LB8017_000_001.png

> [!NOTE]
> 製品バリアントの画像では、分析コード値が空の場合は、ファイル名のキャレットの間に空白が 2 つ必要です。

上の例では、既定のコンフィギュレーションを使用します。 区切り文字と分析コードはコンフィギュレーション可能で、必要な正確な名前付けは展開によって異なる場合があります。 必要な厳密な名前付け規則を識別する方法の 1 つは、ブラウザーの開発者コンソールを使用して、ストアフロントの製品詳細ページ (PDP) で製品分析コードを変更中に製品バリアントの画像要求を検査することです。

## <a name="upload-an-image"></a>画像のアップロード

サイト ビルダーの画像をアップロードするには、次の手順を実行します。

1. 左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。
1. コマンド バーで、**アップロード \> メディア項目のアップロード** を選択します。
1. ファイル エクスプローラー ウィンドウで、アップロードする 1 つまたはそれ以上の画像ファイルに移動して選択し、**開く** を選択します。
1. **メディア項目のアップロード** ダイアログ ボックスで、必要なタイトルと代替テキストを入力します。
1. オプションの説明とキーワードを入力し、必要に応じてカテゴリを選択します。 
1. 画像をアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。
1. **OK** を選択します。

## <a name="upload-a-folder-of-images"></a>画像のフォルダのアップロード

サイト ビルダー内の画像のフォルダを一括アップロードするには、次の手順を実行します。

1. 左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。
1. コマンド バーで、**アップロード \> フォルダのアップロード** を選択します。
1. ファイル エクスプローラー ウィンドウで、アップロードするフォルダに移動して選択し、**開く** を選択します。
1. **メディア項目のアップロード** ダイアログ ボックスで、オプションのキーワードを入力し、必要に応じてカテゴリを選択します。 
1. フォルダをアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします。
1. **OK** を選択します。

## <a name="additional-resources"></a>追加リソース

[資産管理の概要をデジタル化](dam-overview.md)

[ビデオのアップロード](dam-upload-video.md)

[ファイルのアップロード](dam-upload-files.md)

[画像のトリミング](dam-crop-images.md)

[画像の中心のカスタマイズ](dam-custom-focal-point.md)

[静的ファイルのアップロードと提供](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

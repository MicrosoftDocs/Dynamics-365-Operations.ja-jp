---
title: ビデオのアップロード
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーのビデオのアップロード方法について説明します。
author: psimolin
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e3579b54c58898b79c84406480a3b58f541c4621
ms.sourcegitcommit: 257437a57e146496a49782bc8aad179c92fbf6e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2021
ms.locfileid: "6224541"
---
# <a name="upload-videos"></a>ビデオのアップロード

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーのビデオのアップロード方法について説明します。

コマース サイト ビルダーのメディア ライブラリーを使用すると、ビデオをアップロードできます。 イメージの変更コンポーネントを使用すると、さまざまなビューポートとそのブレークポイントに対するビデオが適切に変換されるので、最大速度と解像度でビデオのバージョンをアップロードする必要があります。

### <a name="video-information-specified-during-upload"></a>アップロード中に指定されたビデオ情報

ビデオをアップロードする場合は、次の情報を指定できます。

- **タイトル、説明、キーワード**: ビデオのメタデータ。
- **クローズド キャプションの自動生成**: ビデオに対してクローズド キャプションを自動的に生成するかどうかを指定します (英語のみに対応)。 
- **クローズド キャプション**: 使用するクローズド キャプションを指定します。
- **通常オーディオ**: 使用する通常のオーディオ トラックを指定します。
- **サムネイル**: ビデオのサムネイルを指定します。 指定しない場合は、自動的に生成されます。
- **記述オーディオ**: 使用する記述オーディオ トラックを指定します。

## <a name="upload-a-video"></a>ビデオのアップロード

サイト ビルダー内のビデオをアップロードするには、次の手順を実行します。

1. 左のナビゲーション ウィンドウで、**メディア ライブラリー** を選択します。
1. コマンド バーで、**アップロード \> メディア項目のアップロード** を選択します。
1. ファイル エクスプローラー ウィンドウで、アップロードする 1 つまたはそれ以上のビデオ ファイルに移動して選択し、**開く** を選択します。
1. **メディア項目のアップロード** ダイアログ ボックスで、必要なタイトルと代替テキストを入力します。
1. オプションの説明とキーワードを入力し、必要に応じてカテゴリを選択します。 
1. 画像をアップロードした直後に公開するには、**アップロード後にメディア項目を公開する** チェック ボックスをオンにします
1. **OK** を選択します。

複数のタイプの資産を同時に アップロードしている場合(画像やビデオなど)、**メディア項目のアップロード** ダイアログ ボックスでは、キーワードの指定、アップロード後にファイルをすぐに公開するかどうか、およびビデオ ファイルにクローズ ドキャプションを自動的に生成するかどうかを指定できます。 すべての資産が同じキーワードを共有します。

## <a name="additional-resources"></a>追加リソース

[資産管理の概要をデジタル化](dam-overview.md)

[画像のアップロード](dam-upload-images.md)

[ファイルのアップロード](dam-upload-files.md)

[画像のトリミング](dam-crop-images.md)

[画像の中心のカスタマイズ](dam-custom-focal-point.md)

[静的ファイルのアップロードと提供](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

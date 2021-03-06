---
title: ビデオ プレーヤー モジュール
description: このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: aa1efa6ce959439c49983553edfaf247c8e8dcd5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797410"
---
# <a name="video-player-module"></a>ビデオ プレーヤー モジュール

[!include [banner](includes/banner.md)]

このトピックでは、ビデオ プレーヤー モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

ビデオ プレーヤー モジュールは、ビデオの再生をサポートするために使用されます。 コンテンツ管理システム (CMS) にビデオ コンテンツをアップロードして使用可能であれば、任意のページに追加することができます。 ビデオ プレーヤー モジュールは、.mp4 メディア タイプがサポートしています。

## <a name="video-player-module"></a>ビデオ プレーヤー モジュール

ビデオ プレーヤー モジュールは、E コマース サイト上にビデオを紹介するために使用できます。 再生、一時停止、フルサイズ モード、音声ガイド、クローズド キャプションなど、すべての再生機能がサポートされています。 また、ビデオ プレーヤー モジュールでは、Microsoft のアクセシビリティ標準を満たすための、クローズド キャプションのカスタマイズもサポートしています。 たとえば、フォント サイズや背景色をカスタマイズできます。

ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックもサポートします。 ビデオが CMS にアップロードされると、セカンダリ オーディオ トラックもアップロードできます。 ユーザーが選択した場合、ビデオ プレーヤー モジュールは、セカンダリ オーディオ トラックを再生できます。

### <a name="examples-of-video-player-modules-in-e-commerce"></a>E コマースでのビデオ プレーヤー モジュールの例

- 製品の詳細ページまたはマーケティング ページの説明ビデオ
- プロモーション ビデオまたはマーケティング ページのポリシーに関するビデオ
- 製品の詳細ページまたはマーケティング ページの製品機能を強調するマーケティング ビデオ

以下の図は、ホーム ページにおけるビデオ プレイヤー モジュールの例を示しています。

![ビデオ プレイヤー モジュールの例](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>ビデオ プレーヤー モジュールのプロパティ

| プロパティ名         | 先頭値                               | 説明 |
|-----------------------|-------------------------------------|-------------|
| 自動再生             | **True** または **False**               | 値が **True** に設定されている場合、ビデオは自動的に再生されます。 |
| ミュート                  | **True** または **False**               | 値が **True** に設定されている場合、オーディオはミュートされます。 このプレーヤーの既定値は **False** です。 Chrome ブラウザーでは、自動再生ビデオは既定でミュートになっており、ユーザーがビデオを手動で再生した場合にのみオーディオが再生されます。 |
| ループ                  | **True** または **False**               | 値が **True** に設定されている場合、ビデオはループで繰り返されます。 |
| メディア                 | ビデオ ファイル パスおよび名前 | ビデオ プレーヤーで再生されるビデオ ファイル |
| フルスクリーン再生       | **True** または **False**               | 値が **True** に設定されている場合、ビデオはフルスクリーン モードで再生されます。 |
| 再生/一時停止トリガー    | **True** または **False**               | 値が **True** に設定されている場合、ビデオに再生/一時停止ボタンが表示されます。 |
| ビデオ プレーヤーのコントロール | **True** または **False**               | 値が **True** に設定されている場合は、すべてのビデオ プレーヤー コントロールが表示されます。 これらのコントロールには、再生ボタンと一時停止ボタン、進捗状況インジケーター、およびクローズド キャプション オプションが含まれます。 |
| ポスター画像の非表示     | **True** または **False**               | ビデオにはポスター フレームを含めることができます。 このプロパティの値が **True** に設定されている場合、ポスター フレームは非表示になっています。 |
| マスク レベル            | **0** から **100** までの数字 | スタイル設定のためにビデオに適用されるマスク。 |

## <a name="add-a-video-player-module-to-a-page"></a>ビデオ プレーヤー モジュールをページに追加する

> [!NOTE] 
> ビデオ プレーヤー モジュールを作成する前に、まずビデオをメディア ライブラリにアップロードする必要があります。

新しいページにビデオ プレーヤー モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。

1. **テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。
1. **テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**ビデオプレイヤーのテンプレート** を入力し、**OK**  を選択します。
1. **本文** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。
1. **既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。
1. **コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**ビデオ プレイヤー** モジュールを選択して、**OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。 
1. **ページ** に移動し、**新規** を選択して新たなページを作成します。
1. **テンプレートの選択** ダイアログ ボックスで、作成したビデオ プレイヤーのテンプレートを選択します。 **ページ名** 配下で、 **ビデオ プレイヤーのページ** を入力し、**OK** を選択します。
1. 新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。
1. **コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**ビデオ プレイヤー** モジュールを選択して、**OK** を選択します。
1. ビデオ プレイヤー モジュールのプロパティ ウィンドウで、**ビデオの追加** を選択します。
1. **メディアの選択** ダイアログ ボックスで、ビデオを選択し、**新しいメディア項目のアップロード** を選択します。
1. ファイル エクスプローラーで、1 つ以上のビデオ ファイルを選択し、**開く** を選択します。
1. **メディア項目のアップロード** ダイアログ ボックスで、必要に応じてタイトルとその他の情報を入力し、**OK** を選択します。
1. **メディアの選択** ダイアログ ボックスで、 **閉じる** を選択します。
1. **保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。 ページにビデオ モジュールが表示されます。 その他の設定を変更して、モジュールの動作をカスタマイズすることができます。
1. **編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。 

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[プロモーション バナー モジュール](add-alert.md)

[カルーセル モジュール](add-carousel.md)

[テキスト ブロック モジュール](add-content-rich-block.md)

[コンテンツ ブロック モジュール](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: 既存のサイト ページの変更
description: この記事では、Microsoft Dynamics 365 Commerce で既存のサイト ページを変更する方法について説明します。
author: josaw1
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fb5348c2f29625647f06e48233f877a847677486
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286921"
---
# <a name="modify-an-existing-site-page"></a>既存のサイト ページの変更

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で既存のサイト ページを変更する方法について説明します。

ページを変更する必要がある場合は、最初にページ エディターで開きます。 ページが含まれているサイトに移動し、ページの一覧で目的のページを見つけます。 ページが見つからない場合は、オーサリング ツールのリッチ検索機能が使用できます。 正確なページ名を入力するか、最初のいくつかの文字を入力してから、アスタリスク (\*) を入力します。 フィルタ処理されたページの一覧が表示されます。 この一覧を使用して、目的のページを見つけることができます。 正しいページが見つかったら、ページ名を選択し、ページ エディターでページを開きます。

> [!TIP]
> ページがページインスペクタに表示されている場合は、 **編集** を選択してページをチェックアウトしてから、ページエディタでページを開くことができます。 この方法で、一度に複数のページをチェックアウトできます。

ページ エディターでページを開いたら、そのページがチェック アウトされていることを確認する必要があります。 オーサリング ツールのコマンド バーは、動的で、コンテキストおよび状態に応じて実行されます。 したがって、そのページに対して現在実行できるアクションのみが表示されます。 たとえば、ページがチェック アウトされていない場合、コマンド バーには **保存** と **編集の終了** ボタンが表示されません。 ページの状態は、ウィンドウの右側にも表示されます。

ページがまだチェック アウトされていない場合は、コマンド バーで **編集** を選択します。 コマンド バーを変更して、ページの新しい状態を反映します。 また、このページがユーザーに対してチェック アウトされたことを示す通知が表示されます。

次の手順では、実際の変更を行います。 左のページ アウトライン ツリーを使用して、変更するモジュールを見つけて選択し、右のプロパティ ウィンドウで変更を行うことがよくあります。 

ただし、モデルまたはフラグメントを追加したり、削除したりすることが必要になる場合があります。 フラグメントまたはモジュールを追加するには、ページ アウトライン ツリーを使用して、モジュールまたはフラグメントを追加するスロットを見つけ、省略記号ボタン (**...**) をそのスロットに対して行います。 モジュールまたはフラグメントを追加するコマンドを含むメニューが表示されます。 モジュールまたはフラグメントを削除するには、ページ アウトライン ツリーで目的のモジュールまたはフラグメントを見つけて選択し、省略記号ボタンを選択してから、モジュールまたはフラグメントを削除するコマンドを選択します。

> [!TIP]
> また、直接選択することで、ビジュアル ページ ビルダー プレビューに表示されているモジュールのプロパティを表示および編集することもできます。

変更が完了し、その効果に対するプレビューの完了後、コマンド バーの **編集の終了** を選択して、ページをチェック インする必要があります。 

直ちに変更を発行するには、コマンド バーの **発行** を選択します。 変更したページの最新のチェック イン バージョンが発行され、サイトを表示する外部ユーザーが使用できるようになります。 

## <a name="example-change-the-video-on-the-home-page"></a>例: ホーム ページのビデオを変更

次の例は、ビデオ プレーヤー モジュールに表示されるビデオを変更することによって、ホーム ページを変更する方法を示しています。

1. **サイト** で、**Fabrikam** (またはサイトの名前) を選択します。
1. 左のナビゲーション ウィンドウで、**ページ** を選択します。
1. ホーム ページを検索、選択して、ページ エディターで開きます。
1. コマンド バーで、**編集** を選択します。
1. ページ アウトラインで、**メイン** スロットを選択します。
1. **メイン** スロットの下で、すべての流動的なコンテナー モジュールを展開します。
1. ビデオ プレーヤー モジュールを検索して選択します。
1. 右のプロパティ ウィンドウで、**ビデオ** プロパティを選択します。 資産ピッカーが表示されます。
1. 資産ピッカーで、使用可能なビデオ資産を選択するか、または **新しい資産を更新** を選び、新しいビデオ資産を更新します。
1. **OK** を選択します。
1. **保存** を選択し、**編集完了** を選択します。
1. **コメント** フィールドで、**ビデオを変更した** と入力し、**OK** を選択します。
1. **プレビュー** を選択して、更新されたページをプレビューします。 完了したら、プレビュー タブを閉じて、作成ツールに戻ります。
1. **公開** を選択します。

## <a name="additional-resources"></a>追加リソース

[新しいサイト ページの追加](add-new-page.md)

[ページ レイアウトの選択](select-page-layouts.md)

[SEO メタデータの管理](manage-seo-metadata.md)

[ページの保存、プレビュー、および公開](save-preview-publish-page.md)

[製品ページの拡充](enrich-product-page.md)

[カテゴリ ランディング ページの拡充](enrich-category-page.md)

[ページ コンテンツのアクセシビリティの検証](verify-accessibility.md)

[URL のパラメーターに基いて動的な電子商取引ページを作成する](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: 新しいサイト ページの追加
description: この記事では、Microsoft Dynamics 365 Commerce に新しいサイト ページを追加する方法について説明します。
author: josaw1
ms.date: 02/03/2022
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
ms.openlocfilehash: f6714463c9d5dc844b03f78f0f6ff60c5f270da3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270321"
---
# <a name="add-a-new-site-page"></a>新しいサイト ページの追加

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce に新しいサイト ページを追加する方法について説明します。

サイトのテンプレートとフラグメントを作成したら、次はそれらを使用するページの作成を開始します。 作業を開始するには、テンプレートまたはレイアウト、ページ名、およびページの URL を選択する必要があります。

## <a name="template-or-layout"></a>テンプレートまたはレイアウト

新しいページには、テンプレートまたはレイアウトのいずれかを使用できます。 詳細については、[テンプレートおよびレイアウト](templates-layouts-overview.md) を参照してください。

## <a name="specify-the-page-name"></a>ページの名前を指定します

ページ名は、あなたのサイトに固有のものでなければならず、あなたが簡単に見つけられ、他の人がページの目的を理解できるように、説明的なものにする必要があります。 後でページ名を変更するには、ページを編集してから、プロパティ ペインでページ名の横にあるペン記号を選択します。

## <a name="specify-the-page-url"></a>ページの URL を指定します

新しいページの URL を入力することもできます。 ページを作成するときに、完全な URL を形成するために使用される文字列を入力できます。 この文字列は相対 URL または URL スラッグとも呼ばれます。 次に、URL スラッグに基づいて完全な URL が生成され、新しいページが割り当てられます。 ページを公開する前に URL スラッグを変更することができます。 詳細については、[ページ URL の作成](create-page-URL.md) を参照してください。

> [!NOTE]
> Dynamics 365 Commerce は、URL とコンテンツを切り離します。 つまり、URL に関連付けられていないページを作成し、ページに関連付けられていない URL を作成することができます。 したがって、URL のコンテンツ スワップを実行でき、ダウンタイムを必要とせず、リダイレクトの管理が容易になります。

## <a name="add-a-new-page"></a>新しいページの追加

サイトに新しいサイト ページを追加するには、次のステップを実行します。

1. **サイト** で、**Fabrikam** (またはサイトの名前) を選択します。
1. **新しいページ** を選択します。
1. **新しいページ** ダイアログ ボックスでテンプレートを選択し、**OK** をクリックします。
1. **ページ名** フィールドに、ページの名前 (**新しいページ** など) を入力します。
1. **URL** フィールドに、URL を完了するための文字列 (URL スラグ) を入力します (**mynewpage** など)。
1. **OK** を選択します。 ページ エディターが表示されます。 選択したテンプレートに基づいて、ヘッダーとフッターがページに自動的に追加されます。
1. ページ アウトラインで **メイン** スロットを選択し、省略記号ボタン (**...**) を選択してから、**モジュールの追加** を選択します。
1. **コンテナー** を選択し、**OK** を選択します。
1. **流動的なコンテナー** の省略ボタンを選択し、**モジュールの追加** を選択します。
1. **コンテンツ リッチ ブロック** を選択し、**OK** を選択します。
1. **コンテンツ リッチ ブロック** を選択してから省略ボタンを選択し、**モジュールの追加** を選択します。
1. **コンテンツ リッチ ブロック項目** を選択し、**OK** を選択します。
1. 右側のプロパティ ウィンドウで、**段落** を選択し、フィールドに **テスト テキスト** を入力します。
1. **保存** を選択し、**編集完了** を選択します。
1. **コメント** フィールドで、**追加済の新しいページ** と入力し、**OK** を選択します。
1. **プレビュー** を選択して、ページをプレビューします。 完了したら、プレビュー タブを閉じて、作成ツールに戻ります。
1. **公開** を選択します。
1. ナビゲーション パス (階層リンク) で、**Fabrikam** (またはサイトの名前) を選択します。
1. 左のナビゲーション ウィンドウで、**URL** を選択します。
1. 一覧で URL (**mynewpage**) を検索し、選択します。
1. **公開** を選択します。

## <a name="additional-resources"></a>追加リソース

[既存のサイト ページの変更](modify-existing-page.md)

[ページ レイアウトの選択](select-page-layouts.md)

[SEO メタデータの管理](manage-seo-metadata.md)

[ページの保存、プレビュー、および公開](save-preview-publish-page.md)

[製品ページの拡充](enrich-product-page.md)

[カテゴリ ランディング ページの拡充](enrich-category-page.md)

[ページ コンテンツのアクセシビリティの検証](verify-accessibility.md)

[URL のパラメーターに基いて動的な電子商取引ページを作成する](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

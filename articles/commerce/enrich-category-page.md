---
title: カテゴリ ランディング ページの拡充
description: この記事では、Dynamics 365 Commerce のカテゴリ ページの拡充について説明します。
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: e3397ffee9b32f3d3efedea38255f88daee5233c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282164"
---
# <a name="enrich-a-category-landing-page"></a>カテゴリ ランディング ページの拡充

[!include [banner](includes/banner.md)]

この記事では、Dynamics 365 Commerce のカテゴリ ページの拡充について説明します。

コマースは、カテゴリ データを表示するときに使用される既定のカテゴリのランディング ページを提供します。 既定のカテゴリ ページには、絞り込み条件、分類された製品の配置、並べ替えオプション、選択の概要、ページネーション コントロールなどの必須要素が含まれています。 

ただし、既定のカテゴリ ページを使用する代わりに、コンテンツがより多く、より具体的な要素を持つ「拡充された」カテゴリのランディング ページを使用することもできます。 一般的な拡充には、カテゴリ固有のマーケティング コンテンツをカテゴリ ページに追加することが含まれます。 このコンテンツには、クロスセルを目的としたカテゴリ間の製品配置、編集リスト、画像、ビデオ、およびその他のテキストが含まれる場合があります。 既定のカテゴリ ページを変更するか、特定のカテゴリに対して別のカテゴリ ページを定義することができます。

![拡充されたカテゴリ ランディング ページ。](./media/CategoryLandingPages.png)

Commerce のサイト ビルダーの **製品** ページには、サイトに割り当てられているチャネルのカテゴリの一覧が含まれています。 **拡充** ステータスがカテゴリ ページに選択されている場合は、そのカテゴリ ページは拡充されています。 それ以外の場合、カテゴリには既定のカテゴリ ページとコンテンツが使用されます。 カテゴリ名を選択して、カテゴリの拡充カテゴリ ページと非拡充カテゴリ ページの両方をプレビューできます。

カテゴリ ページを拡充するには、次の操作を行います。

1. **製品** ページで、カテゴリ ページを拡充するカテゴリの名前を選択します。 選択したカテゴリの既定のカテゴリのページが、ページ エディターで開きます。
2. **カテゴリ ページの拡充** を選択します。
3. 拡充したカテゴリ ページのテンプレートを選択します。 マイナーな変更のみを行う場合は、既定のカテゴリ ページを選択できます。 または、特定のカテゴリ ページ テンプレートを選択することもできます。 テンプレートを選択すると、ページ エディターが開き、選択したテンプレートを使用して、選択したカテゴリの新しいカテゴリ ページが作成されます。 ページはチェックアウトされ、変更を加えることができます。

> [!NOTE]
> カテゴリ仕様データを使用するモジュールは、選択したカテゴリのデータを使用します。 選択するテンプレートの設定によって、実行できる変更が決まります。

## <a name="additional-resources"></a>追加リソース

[既存のサイト ページの変更](modify-existing-page.md)

[新しいサイト ページの追加](add-new-page.md)

[ページ レイアウトの選択](select-page-layouts.md)

[SEO メタデータの管理](manage-seo-metadata.md)

[ページの保存、プレビュー、および公開](save-preview-publish-page.md)

[製品ページの拡充](enrich-product-page.md)

[ページ コンテンツのアクセシビリティの検証](verify-accessibility.md)

[URL のパラメーターに基いて動的な電子商取引ページを作成する](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

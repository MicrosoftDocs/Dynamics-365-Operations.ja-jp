---
title: URL パラメーターに基づく動的な eコマース ページの作成
description: この記事では、URL のパラメーターに基づいて動的なコンテンツを提供できる Microsoft Dynamics 365 Commerce の電子商取引ページの設定方法について説明します。
author: bicyclingfool
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: 718bc099347f2924b299ccd4562d9d7055c43187
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282879"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>URL パラメーターに基づく動的な eコマース ページの作成

[!include [banner](includes/banner.md)]

この記事では、URL のパラメーターに基づいて動的なコンテンツを提供できる Microsoft Dynamics 365 Commerce の電子商取引ページの設定方法について説明します。

電子商取引のページは、URL パスのセグメントに基づいて、異なるコンテンツを提供するよう構成できます。 したがって、このページは動的ページと呼ばれます。 セグメントは、ページ内容を取得するパラメーターとして使用されます。 たとえば、サイト ビルダーで作成され **ブログ\_ビューアー** という名前のページは、URL (`https://fabrikam.com/blog`) にマッピングされます。 このページを使用すると、URL パスの最後のセグメントに基づいた異なるコンテンツを表示できます。 たとえば、URL (`https://fabrikam.com/blog/article-1`) の最後のセグメントは **article-1** です。

パラメータ化された URL セグメントは、サイト ビルダ ページで上書きすることもできます。 たとえば、サイト ビルダーで作成され **ブログ\_概要** という名前のページは、URL (`https://fabrikam.com/blog/about-this-blog`) にマッピングできます。 末尾の  `/about-this-blog`セグメントで `https://fabrikam.com/blog` URL が要求された場合、その `https://fabrikam.com/blog` ページで使用される `/about-this-blog` パラメータとして解釈される区分ではなく、**ブログ\_概要** ページのコンテンツが返されます。 

動的ページに渡すパラメータの名前を選択した場合、URL に表示される動的ページの名前 (`/blog` 前の例の) は、パラメータ名またはパラメータ名のサブサイトとして使用できません。 

> [!NOTE]
> 動的なページ コンテンツをホスト、取得、表示する機能は、カスタム モジュールを使用して実装されます。 詳細については、[オンライン チャンネルの拡張性](e-commerce-extensibility/overview.md)を参照してください。

## <a name="set-up-a-dynamic-e-commerce-page"></a>動的な電子商取引ページを設定する

動的な電子商取引のページを設定するには、動的なページを作成し、ベースとなる URL を作成し、動的なページへの経路を設定する必要があります。

### <a name="create-the-page-that-will-serve-dynamic-content"></a>動的なコンテンツを提供するページの作成

動的なコンテンツを提供するページを作成するには[新しいサイト ページを追加する ](add-new-page.md)に記載の手順に従います 。 作成するページには、URL パスの最後のセグメントを使用して外部データ ソースからコンテンツを取得するモジュールの実装が必要です。 カスタム モジュール開発の詳細については、[オンライン チャンネルの機能拡張](e-commerce-extensibility/overview.md) を参照してください。

### <a name="create-the-base-url-for-the-dynamic-page"></a>動的なページのベース URL を作成する

Commerce サイト ビルダーで動的ページのベース URL を作成するには、次の手順に従います。

1. **URL** に移動し、**新規 \>新規 URL** を選択します。
1. **新規 URL の作成** ダイアログ ボックスで、**内部 ページ** を選択します。 **URL パス** で、動的ページのルートとして使用するパス を入力します (この例では、**/blog**) です。 その後、**次へ** を選択します。
1. **ページの選択** ダイアログ ボックスで、動的ページとして作成したページを選択し、**保存** を選択します。
1. **公開** を選択します。

### <a name="configure-the-route-to-the-dynamic-page"></a>動的ページへの経路を構成する

Commerce サイト ビルダーで動的ページへの経路を構成するには、次の手順に従います。

1. **サイト 設定 \> 拡張機能** に移動します。
1. **パラメーター化された URL パス** で、**追加** を選択し、URL の作成時に入力した URL パス (この例では **/blog**) を入力します。
1. **保存と公開** を選択します。

経路を構成した後は、パラメーター化した URL パスへのすべてのリクエストは、その URL に関連付けられているページが返されます。 追加のセグメントが含まれるリクエストがある場合は、関連するページが返され、その区分をパラメータとして使用してページのコンテンツが取得されます。 たとえば、`https://fabrikam.com/blog/article-1` は、**/article-1** パラメーターを使用して取得されるるコンテンツを表示する `https://fabrikam.com/blog` ページが返されます。

## <a name="override-a-parameterized-url-with-a-custom-page"></a>パラメーター化された URL をカスタム ページで上書きする

パラメータ化された URL を Commerce サイト ビルダのカスタム ページで上書きするには、次の手順に従います。

1. **URL** に移動し、**新規 \>新規 URL** を選択します。
1. **新規 URL の作成** ダイアログ ボックスで、**内部 ページ** を選択します。 **URL パス** で、上書きするセグメントを含むパスを入力します (この例では、**/blog/about-this-blog**)。 その後、**次へ** を選択します。
1. **ページ の選択** ダイアログ ボックスで、カスタム ページを選択し、**保存** を選択します。
1. **公開** を選択します。
1. カスタム ページがまだ公開されていない場合は、**ページ** に移動し、カスタム ページを選択して、**公開** を選択します。

カスタム ページが公開された後は、コンテンツをパラメータ化した動的ページではなく、カスタム ページが表示されます。

## <a name="additional-resources"></a>追加リソース

[既存のサイト ページの変更](modify-existing-page.md)

[新しいサイト ページの追加](add-new-page.md)

[ページ レイアウトの選択](select-page-layouts.md)

[SEO メタデータの管理](manage-seo-metadata.md)

[ページの保存、プレビュー、および公開](save-preview-publish-page.md)

[製品ページの拡充](enrich-product-page.md)

[カテゴリ ランディング ページの拡充](enrich-category-page.md)

[ページ コンテンツのアクセシビリティの検証](verify-accessibility.md)

[オンライン チャネルの拡張性](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

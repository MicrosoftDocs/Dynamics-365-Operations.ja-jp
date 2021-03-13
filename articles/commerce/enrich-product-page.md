---
title: 製品ページの拡充
description: このトピックでは、Microsoft Dynamics 365 Commerce で製品ページを拡充する方法について説明します。
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fcb8eda188a6796282a7a800b87a68dfef9d7d62
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097341"
---
# <a name="enrich-a-product-page"></a>製品ページの拡充


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で製品ページを拡充する方法について説明します。

## <a name="overview"></a>概要

既定では、サイトは汎用ページを使用して製品データを表示します。 このページには、製品とその販売に必要なコントロールに関する基本的な情報が含まれています。 ただし、特定の製品の追加画像またはテキストを使用して、Commerce Scale Unit から取得した情報を補足することができます。 このプロセスは、製品ページの拡充と呼ばれます。

多くの場合、製品に特定の追加コンテンツを使用する必要があります。 オーサリング ツールで **Retail と Commerce** にアクセスすると、サイトに割り当てられているチャネルの製品の一覧が表示されます。 この一覧の **拡充** 列は、製品の製品ページが拡充されているかどうかを示しています。 列にチェック マークが表示される場合は、製品に対して拡充された製品ページが存在します。 チェック マークが表示されない場合は、製品に対して既定の製品ページとコンテンツが使用されます。 一覧で製品名を選択して、拡充された製品ページと非拡充の製品ページの両方をプレビューできます。

## <a name="enrich-a-product-page"></a>製品ページの拡充

製品ページを拡充するには、次の手順に従います。

1. **サイト** で、**Fabrikam** (またはサイトの名前) を選択します。
1. 左のナビゲーション ウィンドウで、**製品** を選択します。
1. 拡充された製品ページがない製品を選択します。
1. アクション ウィンドウで、**製品ページの拡充** を選択します。
1. **PDP テンプレート** を選択し、**OK** を選択します。
1. 左側のページのアウトライン ツリーで、**メイン** スロットを展開します。
1. **メイン** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **コンテナー 2** を選択し、**OK** を選択します。
1. **コンテナー 2** の省略ボタンを選択し、**モジュールの追加** を選択します。
1. **機能** を選択し、**OK** を選択します。
1. 右側のプロパティ ウィンドウの **リッチ テキスト** フィールドに、更新された製品の説明を入力します。
1. **ヘッダー** フィールドに、ヘッダーのテキストを入力してから **OK** を選択します。
1. **保存** を選択し、**編集完了** を選択します。
1. **コメント** フィールドに、**製品を拡充した** と入力し、**OK** を選択します。
1. **プレビュー** を選択して、拡充された製品ページをプレビューします。 完了したら、プレビュー タブを閉じて、作成ツールに戻ります。
1. **公開** を選択します。

## <a name="additional-resources"></a>追加リソース

[既存のサイト ページの変更](modify-existing-page.md)

[新しいサイト ページの追加](add-new-page.md)

[ページ レイアウトの選択](select-page-layouts.md)

[SEO メタデータの管理](manage-seo-metadata.md)

[ページの保存、プレビュー、および公開](save-preview-publish-page.md)

[カテゴリ ランディング ページの拡充](enrich-category-page.md)

[ページ コンテンツのアクセシビリティの検証](verify-accessibility.md)

[URL のパラメーターに基いて動的な電子商取引ページを作成する](create-dynamic-pages.md)

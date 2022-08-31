---
title: ページ集計モジュール
description: この記事では、ページ集計モジュールと、これを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。
author: samjarawan
ms.date: 04/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 1cd91613255e896e96799a64c0a264491b38d6d6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281412"
---
# <a name="page-summary-modules"></a>ページ集計モジュール

[!include [banner](includes/banner.md)]

この記事では、ページ集計モジュールと、これを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。

ページ集計モジュールは、検索エンジンやソーシャル共有サイトが使用できるページ集計メタ データの入力を簡略化するのに役立ちます。 このメタデータには正規化されたリンクが含まれます。

Dynamics 365 Commerce モジュール ライブラリには、ページ集計、カテゴリ ページ集計、リスト ページ集計、および製品ページ集計のモジュールなど、複数のページ集計モジュールが含まれています。 各ページ集計モジュールには、そのモジュールが使用される特定のページ タイプを対象とする検索エンジン最適化 (SEO) メタデータがあります。 すべての集計ページ モジュールは、次のセクションで説明するのと同じプロパティ セットを共有します。

> [!NOTE]
> Commerce モジュール ライブラリ バージョン 9.27 以上に含まれている製品ページの集計モジュールは、[Schema.org の製品スキーマ](https://schema.org/Product) を使用して、JSON 形式の基本的な製品メタデータをページのヘッダー セクションに挿入しています。 このメタデータは、購入ボックス モジュールおよび他の製品ページ メタデータで使用されるのと同じ Commerce Runtime (CRT) API データ アクションを使用して自動的に生成されます。 多くの場合、製品メタデータで構成されている Schema.org は、主要な検索エンジンが豊富な検索結果を表示するために使用されます。 既定では、製品ページの集計モジュールには、製品名、製品の説明、オファー (通貨および価格決定) 情報、および Schema.org の製品スキーマ仕様ごとの既定の画像の場所が含まれます。 必要に応じて、このモジュールと使用されるデータ アクションを Commerce オンライン SDK を使用して拡張し、メタデータ要件を強化または変更できます。


## <a name="summary-page-module-properties"></a>集計ページ モジュール プロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| 肩書き | テキスト | サイト ページのタイトル。 |
| 説明 | テキスト | サイト ページの内容の簡単な説明。 |
| キーワード | テキスト | サイト ページに関連する一連のコンマ区切りのキーワード。 |
| Twitter タグの無効化 | **True** または **False** | このプロパティが **True** に設定されている場合、HTML で Twitter タグは表示されません。 |
| 画像の共有 | 使用できる画像の一覧で選択された画像 | サイト ページが共有されている場合に使用する画像。 |
| Facebook OG タグの無効化 | **True** または **False** | このプロパティが **True** に設定されている場合、HTML で Facebook Open Graph (OG) タグは表示されません。 |
| アプリケーション設定で指定された接頭語と接尾語を無視する | **True** または **False** | このプロパティが **True** に設定されている場合、サイト レベルの接頭語と接尾語の設定は無視されます。 |

## <a name="add-a-page-summary-module-to-a-template"></a>テンプレートへのページ集計モジュールの追加

テンプレートにページ集計モジュールを追加するには、次の手順に従います。

1. サイトのコマース サイト ビルダで、**テンプレート** を選択します。
1. テンプレートを選択し、**編集** を選択します。
1. **HTML ヘッド** スロットで省略 (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**ページ集計モジュール** (または、**リスト ページ集計** などの、別のページ集計モジュール) を選択し、**OK** を選択します。 テンプレートを使用するページ タイプ用の適切なページ集計モジュールが追加されていることを確認してください。

    ![新しいモジュールの追加。](media/page-summary-1.png)

集計モジュールを追加した後、次の図の例のようになります。 これでモジュールが構成され、テンプレートを保存および公開できます。

![追加されたページ集計モジュール。](media/page-summary-2.png)

> [!NOTE]
> テンプレートで既定値を設定できますが、これらの値はテンプレートを使用するページ上で上書きできます。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[既定のページ モジュール](default-page-module.md)

[外部およびインライン スクリプト モジュール](script-module.md)

[メタタグ モジュール](metatags-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

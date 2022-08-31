---
title: 既定のページ モジュール
description: この記事では、既定のページ モジュールと、これを Microsoft Dynamics 365 Commerce のページ テンプレートに追加する方法について説明します。
author: samjarawan
ms.date: 05/18/2022
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
ms.openlocfilehash: 03868a979b3444f438797ea2a8ce0f44d9cd8e25
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273570"
---
# <a name="default-page-module"></a>既定のページ モジュール

[!include [banner](includes/banner.md)]

この記事では、既定のページ モジュールと、これを Microsoft Dynamics 365 Commerce のページ テンプレートに追加する方法について説明します。

既定のページ モジュールは、ページのルート コンテナーとなる特別なモジュールで、テンプレートの **本文** スロットにのみ追加できます。 既定のページ モジュールは、次の例に示すように、コマース サイト ビルダ ページ エディターに表示されるコア スロット (**ヘッダー スロット**、**サブ ヘッダー スロット**、**メイン スロット**、**サブフッター スロット**、および **フッター スロット**) を定義します。

![ページ モジュール スロット。](media/page-module-1.png)

コマース モジュール ライブラリは、既定のページ モジュールの 1 つのタイプのみを提供します。 ただし、 [コマース オンライン チャンネル機能拡張ソフトウェア開発キット (SDK)](e-commerce-extensibility/overview.md) を使用して、必要に応じて追加のカスタムの既定のページ モジュールを作成できます。

## <a name="page-module-properties"></a>ページ モジュール プロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| [メイン コンテキストへスキップ] のテキスト | テキスト | ページの「メイン コンテンツにスキップ」リンクに表示されるリンク テキスト。 既定値は **メイン コンテンツ にスキップ** です。 |
| テーマ | 使用できるテーマの一覧で選択されたテーマ | このテンプレートから派生されたページに使用するテーマ。<p><strong> 注: </strong> このプロパティは非推奨になり、将来のリリースで削除されます。 テーマは、サイト レベルでのみ設定する必要があります。</p> |
| サインインが必要ですか? | **True** または **False** | このブール値プロパティは、ページへのアクセスにユーザーのサインインが必要かどうかを制御します。 **True** に設定されている場合、サインインしていないユーザーはサインイン ページにリダイレクトされます。 |

## <a name="add-a-default-page-module-to-a-template"></a>テンプレートへの既定ページ モジュールの追加

テンプレートに既定ページ モジュールを追加するには、次の手順に従います。

1. サイトのコマース サイト ビルダで、**テンプレート** を選択します。
1. テンプレートを選択し、**編集** を選択します。
1. **本文** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。

    ![新しいモジュールの追加。](media/page-module-2.png)

1. **モジュールの選択** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。

    ![既定のページ モジュールを追加します。](media/page-module-3.png)

既定のページ モジュールを追加した後、次の図の例のようになります。 これでモジュールが構成され、テンプレートを保存および公開できます。

![既定のページ モジュールが追加されました。](media/page-module-4.png)

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[ページ集計モジュール](page-summary-module.md)

[外部およびインライン スクリプト モジュール](script-module.md)

[メタタグ モジュール](metatags-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

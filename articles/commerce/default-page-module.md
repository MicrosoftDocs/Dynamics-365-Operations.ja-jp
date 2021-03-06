---
title: 既定のページ モジュール
description: このトピックでは、既定のページ モジュールと、これを Microsoft Dynamics 365 Commerce のページ テンプレートに追加する方法について説明します。
author: samjarawan
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 18be8e54cd85c3443bd53c928280e623c517b374
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020693"
---
# <a name="default-page-module"></a>既定のページ モジュール

[!include [banner](includes/banner.md)]

このトピックでは、既定のページ モジュールと、これを Microsoft Dynamics 365 Commerce のページ テンプレートに追加する方法について説明します。

既定のページ モジュールは、ページのルート コンテナーとなる特別なモジュールで、テンプレートの **本文** スロットにのみ追加できます。 既定のページ モジュールは、次の例に示すように、コマース サイト ビルダ ページ エディターに表示されるコア スロット (**ヘッダー スロット**、**サブ ヘッダー スロット**、**メイン スロット**、**サブフッター スロット**、および **フッター スロット**) を定義します。

![ページ モジュール スロット](media/page-module-1.png)

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

    ![新しいモジュールの追加](media/page-module-2.png)

1. **モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。

    ![既定のページ モジュールの追加](media/page-module-3.png)

既定のページ モジュールを追加した後、次の図の例のようになります。 これでモジュールが構成され、テンプレートを保存および公開できます。

![既定のページ モジュールが追加された](media/page-module-4.png)

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[ページ集計モジュール](page-summary-module.md)

[外部およびインライン スクリプト モジュール](script-module.md)

[メタタグ モジュール](metatags-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

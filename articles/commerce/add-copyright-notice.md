---
title: 著作権に関する注意事項の追加
description: このトピックでは、E コマース Web サイトに著作権に関する注意事項を追加する方法について説明します。
author: psimolin
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39135a2eca25336097ee9eddf06dc6709c102571
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696948"
---
# <a name="add-a-copyright-notice"></a>著作権に関する注意事項の追加

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、E コマース Web サイトに著作権に関する注意事項を追加する方法について説明します。

## <a name="prerequisites"></a>必要条件

サイトに著作権に関する注意事項を追加する前に、次の項目が必要です。

- 共有フッター フラグメントを含むテンプレート。
- そのテンプレートを使用するページ。

## <a name="add-a-copyright-notice"></a>著作権に関する注意事項の追加

特定のテンプレートを使用する各ページの下に著作権に関する注意事項を追加するには、次の手順を実行します。

1. **フラグメント**に移動し、**新しいページ フラグメント**を選択します。
1. ダイアログ ボックスで、**フッター** モジュールを選択し、フラグメントに名前を付けます。 たとえば、**フッター 著作権** と入力します。
1. **OK** を選択します。
1. ナビゲーション ウィンドウで、**フッター**の横にある省略記号ボタン (**...**) を選択してから、**モジュールの追加**を選択します。
1. ダイアログ ボックスで、**フッター カテゴリ**を選択し、**OK** を選択します。
1. ナビゲーション ウィンドウで、**フッター カテゴリ**の横にある省略記号ボタンを選択してから、**モジュールの追加**を選択します。
1. ダイアログ ボックスで、**コンテンツ リッチ ブロック項目**を選択し、**OK** を選択します。
1. ナビゲーション ウィンドウで、**コンテンツ リッチ ブロック項目**を選択します。
1. 右側のプロパティ ウィンドウの、**段落**フィールドで、著作権に関するメッセージを追加します。 たとえば、**(C) Fabrikam 2019** と入力します。
1. **保存**を選択し、**チェックイン**を選択してから、**公開**を選択します。
1. **テンプレート**に移動し、テンプレートを選択してから、**チェックアウト**を選択します。
1. **ページ アウトライン**で、**本文**を展開してから、**既定のページ**を展開します。
1. **フッター スロット**の横にある省略記号ボタンを選択し、**フラグメントの追加**を選択します。
1. 前に作成したフラグメントを選択し、**選択**を選択します。
1. テンプレートをチェックインし、公開します。

著作権に関する注意事項を含むフッターは、選択したテンプレートを使用するすべてのページの下部に自動的に表示されます。

## <a name="additional-resources"></a>追加リソース

[ロゴの追加](add-logo.md)

[サイト テーマの選択](select-site-theme.md)

[お気に入りの追加](add-favicon.md)

[ようこそメッセージの追加](add-welcome-message.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)


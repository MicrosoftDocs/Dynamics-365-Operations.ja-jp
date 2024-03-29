---
title: 著作権に関する注意事項の追加
description: この記事では、E コマース Web サイトに著作権に関する注意事項を追加する方法について説明します。
author: josaw1
ms.date: 10/16/2020
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
ms.openlocfilehash: 044fdd958a7233322553c8d9b03163c6ce5c4cb3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270458"
---
# <a name="add-a-copyright-notice"></a>著作権に関する注意事項の追加

[!include [banner](includes/banner.md)]

この記事では、E コマース Web サイトに著作権に関する注意事項を追加する方法について説明します。

## <a name="prerequisites"></a>必要条件

サイトに著作権に関する注意事項を追加する前に、次の項目が必要です。

- 共有フッター フラグメントを含むテンプレート。
- そのテンプレートを使用するページ。

## <a name="add-a-copyright-notice"></a>著作権に関する注意事項の追加

特定のテンプレートを使用する各ページの下に著作権に関する注意事項を追加するには、次の手順を実行します。

1. **フラグメント** に移動し、**新規** を選択します。
1. **新規フラグメント** ダイアログ ボックスで、**フッター** モジュールを選択し、フラグメントに名前を付けます。 たとえば、**フッター 著作権** と入力します。
1. **OK** を選択します。
1. ナビゲーション ウィンドウで、**フッター** の横にある省略記号ボタン (**...**) を選択してから、**モジュールの追加** を選択します。
1. ダイアログ ボックスで、**フッター カテゴリ** を選択し、**OK** を選択します。
1. ナビゲーション ウィンドウで、**フッター カテゴリ** の横にある省略記号ボタンを選択してから、**モジュールの追加** を選択します。
1. ダイアログ ボックスで、**テキスト ブロック** を選択し、**OK** を選択します。
1. 左のナビゲーション ウィンドウで、**テキスト ブロック** を選択します。
1. 右側のプロパティ ウィンドウの、**段落** フィールドで、著作権に関するメッセージを追加します。 たとえば、**(C) Fabrikam 2019** と入力します。
1. **保存** を選択し、**編集を終了する** を選択し、続いて **公開** を選択します。
1. **テンプレート** に移動し、テンプレートを選択してから、**編集** を選択します。
1. **ページ アウトライン** で、**本文** を展開してから、**既定のページ** を展開します。
1. **フッター スロット** の横にある省略記号ボタンを選択し、**フラグメントの追加** を選択します。
1. 前に作成したフラグメントを選択し、**選択** を選択します。
1. **編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。

著作権に関する注意事項を含むフッターは、選択したテンプレートを使用するすべてのページの下部に自動的に表示されます。

## <a name="additional-resources"></a>追加リソース

[ロゴの追加](add-logo.md)

[サイト テーマの選択](select-site-theme.md)

[CSS 上書きファイルの作業](css-override-files.md)

[ファビコンの追加](add-favicon.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: イメージ リスト モジュール
description: このトピックでは、イメージ リスト モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 485d0714927cef5a292fd1beee826a90e9233e35
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479492"
---
# <a name="image-list-module"></a>イメージ リスト モジュール

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、イメージ リスト モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

イメージ リスト モジュールは、サイト ページに画像のコレクション (配列) を簡単に追加するために使用できます。 配列内の各画像は、段落テキストとリンク URL を使用して構成できます。 イメージ リスト モジュールは、ブランド ロゴやロゴを含む一覧を表示する場合に最適です。

> [!IMPORTANT]
> - イメージ リスト モジュールは、Dynamics 365 Commerce バージョン 10.0.20 リリース時点で、Commerce モジュール ライブラリで使用できます。
> - イメージ リスト モジュールは Adventure Works のテーマで示されています。

次の図は、イメージ リスト モジュールが Adventure Works の企業と顧客間 (B2C) サイト ページで、ロゴを含むテキストの一覧を表示する例を示しています。

![ロゴを含むテキストの一覧を表示するイメージ リスト モジュールの例](./media/Image_list.PNG)

次の図は、イメージ リスト モジュールが Adventure Works の企業と顧客間 (B2B) サイト ページで、ブランド ロゴを表示する例を示しています。

![ブランド ロゴを表示するイメージ リスト モジュールの例](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>イメージ リスト モジュールのプロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| ヘッダー       | ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**) | イメージ リスト モジュールのテキスト ヘッダーです。 |
| イメージ リスト    | 画像、テキスト、および URL | 配列内の各品目は、段落テキストと URL が伴う画像です。 |

## <a name="add-an-image-list-module-to-a-new-page"></a>イメージ リスト モジュールを新しいページに追加する

新しいページにイメージ リスト モジュールを追加して、Commerce のサイト ビルダーに必要なプロパティを設定するには、次の手順を実行します。

1. **テンプレート** に移動し、サイトのホーム ページのマーケティング テンプレートを開きます (または、新しいマーケティング テンプレートを作成します)。
1. 既定のページの **メイン** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**イメージ リスト** モジュールを選択して、**OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。
1. **ページ** に移動し、サイトのホーム ページを開きます (または、マーケティング テンプレートを使用して新しいホーム ページを作成します)。
1. 既定のページの **メイン** スロットで、省略記号ボタン (**...**) を選択してから、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**イメージ リスト** を選択して、**OK** を選択します。
1. イメージ リスト モジュールのプロパティ ウィンドウで、ヘッダーを追加します (例 : **ブランド**)。
1. イメージ リスト品目を追加し、画像、一部の段落テキスト、およびリンク先 URL を指定します。
1. 必要に応じて、イメージ リスト モジュールを追加および構成します。
1. **保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。
1. **編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[Adventure Works テーマ](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

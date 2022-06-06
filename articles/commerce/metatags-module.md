---
title: メタタグ モジュール
description: このトピックでは、メタタグ モジュールと、それらを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。
author: samjarawan
ms.date: 05/18/2022
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
ms.openlocfilehash: 45610e8c86847300f9fa835ed9a6b4269eef72c0
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780778"
---
# <a name="metatags-module"></a>メタタグ モジュール

[!include [banner](includes/banner.md)]

このトピックでは、メタタグ モジュールと、それらを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。

メタタグ モジュールは、サイト ページの検索エンジンの最適化 (SEO) ランキングの向上に役立つカスタム HTML メタ タグの入力をサポートします。

メタタグ モジュールは、テンプレートの **HTML ヘッド** スロットに追加されます。 その後、テンプレートとテンプレートから派生したサイト ページの両方で構成できるようになります。

1 つ以上の一般メタ タグをテンプレートに追加できます。 ただし、ページ固有のメタ タグは関連するサイト ページに追加される必要があります。 ページ レベルのメタ タグは、テンプレート レベルのメタ タグを上書きします。 

次の図は、メタ タグモジュールがテンプレートの **HTML ヘッド** スロットに追加された例を示しています。

![テンプレートの HTML ヘッド スロットに含まれるメタタグ モジュール。](media/metatags-module-1.png)

## <a name="metatags-module-properties"></a>メタタグ モジュールのプロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| メタ タグ | テキスト | 1 つ以上のメタ タグをモジュールに追加できます。 |

## <a name="add-a-metatags-module-to-a-template"></a>テンプレートへのメタ タグ モジュールの追加

テンプレートに メタタグ モジュールを追加するには、次の手順に従います。

1. サイトのコマース サイト ビルダで、**テンプレート** を選択します。
1. テンプレートを選択し、**編集** を選択します。
1. **HTML ヘッド** スロットで省略 (**...**) を選択し、**モジュールの追加** を選択します。

    ![新しいモジュールの追加。](media/metatags-module-2.png)

1. **モジュールの選択** ダイアログ ボックスで **メタタグ** モジュールを選択して、**OK** を選択します。

    ![メタタグ モジュールを追加します。](media/metatags-module-3.png)

1. メタ タグを追加するには **メタタグ** スロットを選択します。 次に、モジュールのプロパティ ウィンドウで、**メタ タグの追加** を選択して各メタ タグを追加します。 上矢印ボタンと下矢印ボタンを使用して、メタ タグの順序を変更できます。
1. テンプレートの編集が完了したら、**保存** を選択し、**編集の完了** を選択して、**発行** を選択して公開します。

テンプレートにメタ タグ モジュールを追加した後、ページ固有のメタ タグをテンプレートを使用するサイトページに追加できます。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[既定のページ モジュール](default-page-module.md)

[ページ集計モジュール](page-summary-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

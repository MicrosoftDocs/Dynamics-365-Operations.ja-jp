---
title: IFRAME​​ モジュール
description: このトピックでは、iframeモジュールを使用して、Microsoft Dynamics 365 Commerceでサイトのページに追加する方法を説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b7b5935a81377e0cb6acfc497eece6148bf1eeee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993372"
---
# <a name="iframe-module"></a>IFRAME​​ モジュール

[!include [banner](includes/banner.md)]

このトピックでは、iframeモジュールを使用して、Microsoft Dynamics 365 Commerceでサイトのページに追加する方法を説明します。

## <a name="overview"></a>概要

iframe モジュールは、サイトの外部コンテンツをホストする iframe (インライン フレーム) を提供します。 たとえば、どのサイトのページでも YouTube の動画や PDF ファイル ビューアをホストすることができます。 

iframe モジュールにはターゲットの URL が必要となります。 そして、HTML の **iframe** 要素の中にターゲット ページのコンテンツをホストします。 外部 URL は、サイトのコンテンツ セキュリティポリシー (CSP) の指示に従って、許可リストに登録されている必要があります。 iframe のコンテンツでは、**frame-ancestor** のディレクティブを使用して URL を許可する必要があります。 詳細については、[コンテンツ セキュリティ  ポリシー (CSP) の管理](manage-csp.md)を参照してください。

> [!NOTE]
> iFrame モジュールは、Dynamics 365 Commerce 10.0.13 リリースで利用可能です。

以下の画像は、サイトページに外部動画を表示する iframe モジュールの例です。

![外部動画を表示する iframe モジュールの例](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>iframe モジュールのプロパティ

| プロパティ名             | 先頭値                 | 説明 |
|---------------------------|-----------------------|-------------|
| ヘッダー | テキスト | モジュールのヘッダー。 |
| ターゲット URL | URL | モジュール内でホストされている URL。 |
| Height | 数値またはパーセンテージ | モジュールの高さをピクセル、パーセンテージで指定します。 たとえば、値が **100** の場合はピクセル数として扱われ、値が **100%** の場合はパーセンテージとして扱われます。 |
| aria ラベル | テキスト | アクセシビリティを実現する目的で、Accessible Rich Internet Applications (ARIA) ラベルを定義することができます。 |

## <a name="add-an-iframe-module-to-a-page"></a>iFrame モジュールをページに追加する

iframe モジュールをページに追加して外部動画を表示するには、以下の手順に従ってください。

1. **テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。
1. **テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、**マーケティング テンプレート** を入力し、**OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。
1. **ページ** に移動し、**新規** を選択して新たなページを作成します。
1. **テンプレートの選択** ダイアログ ボックスで、**マーケティング テンプレート** のテンプレートを選択します。 **ページ名** 配下で、**マーケティング ページ** と入力し、**OK** を選択します。
1. 新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。
1. モジュールのプロパティ ウィンドウで、**幅** の値を **全コンテナー** に設定します。
1. **コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの追加** ダイアログ ボックスで、**iframe** モジュールを選択し、**OK** を選択します。
1. モジュールのプロパティ ペインで、動画に使用する外部 URL を **ターゲット URL** に設定します。
1. 必要に応じて、 **ヘッダー** や **高さ** などのプロパティを設定します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。
1. ご利用のサイトのマーケティング ページに移動します。 動画が iframe モジュールでレンダリングされていることが確認できます。
 
## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[コンテンツ セキュリティ ポリシー (CSP) の管理](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
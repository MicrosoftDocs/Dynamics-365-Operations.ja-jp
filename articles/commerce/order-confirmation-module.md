---
title: 注文確認モジュール
description: このトピックでは、注文確認モジュールおよび Microsoft Dynamics 365 Commerce での作成方法について説明します。
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698329"
---
# <a name="order-confirmation-module"></a>注文確認モジュール

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、注文確認モジュールおよび Microsoft Dynamics 365 Commerce での作成方法について説明します。

## <a name="overview"></a>概要

注文確認モジュールは、注文の完了後に注文確認のページに確認メッセージを表示するために使用されます。 注文確認モジュールは、注文確認書番号およびチェックアウト時に指定された顧客の電子メール アドレスを表示します。

注文がチェックアウト中に配置されると、注文の確認書番号および顧客の電子メールアドレスが、ページの URL のクエリ文字列として注文確認ページに渡されます。 注文の確認モジュールは、この情報を受け取り、注文の確認ページに注文状態を表示します。 注文確認モジュールでは、このページのコンテキストを使用して注文状態を指定する必要があります。

## <a name="order-confirmation-module-properties"></a>注文確認モジュールのプロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| ヘッダー       | ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**) | 注文確認モジュールには、ヘッダーを付けることができます。 既定では、**H2** ヘッダー タグがヘッダーに使用されます。 ただし、アクセシビリティ要件を満たすようにタグを変更できます。 |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>注文確認ページのモジュールで使用可能なモジュール 

- **推奨** - 推奨モジュールを注文確認ページに追加して、顧客に他の製品を提案することができます。
- **マーケティング** - マーケティング モジュールは、注文確認ページにマーケティングのコンテンツを追加することができます。

## <a name="create-an-order-confirmation-page-module"></a>注文確認ページのモジュールの作成

1. **注文確認のテンプレート**という名前のページ テンプレートを作成します。
1. 既定ページの**メイン**スロットで、注文確認モジュールを追加します。
1. 注文確認モジュールで、推奨モジュールを追加します。
1. テンプレートを保存およびプレビューします。 注文確認番号のコンテキストを必要とするため、注文確認モジュールは表示されないようにする必要があります。
1. テンプレートをチェックインし、公開します。
1. 作成した注文確認テンプレートを使用して、**注文確認ページ**という名前のページを作成します。
1. 既定のページをページ アウトラインに追加します。
1. **ヘッダー**スロットで、ヘッダー フラグメントを追加します。
1. **フッター**スロットで、フッター フラグメントを追加します。
1. **メイン**スロットで、注文確認モジュールを追加します。
1. 注文確認モジュールのプロパティ ウィンドウで、見出しの**注文確認**を追加します。
1. 注文確認モジュールの下で、推奨モジュールを追加し、**新規**および**ベストセラー**設定を使用するように構成します。
1. ページを保存およびプレビューし、チェック イン後に発行します。

## <a name="additional-resources"></a>追加リソース

[スタート キットの概要](starter-kit-overview.md)

[コンテナー モジュール](add-container-module.md)

[購入ボックス モジュール](add-buy-box.md)

[カート モジュール](add-cart-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[ヘッダーモジュール](author-header-module.md)

[フッター モジュール](author-footer-module.md)

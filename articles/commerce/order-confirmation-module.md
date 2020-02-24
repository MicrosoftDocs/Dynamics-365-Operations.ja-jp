---
title: 注文詳細のモジュール
description: このトピックでは、注文詳細モジュールおよび Microsoft Dynamics 365 Commerce での使用方法について説明します。
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026020"
---
# <a name="order-details-module"></a>注文詳細のモジュール


[!include [banner](includes/banner.md)]

このトピックでは、注文詳細モジュールおよび Microsoft Dynamics 365 Commerce での使用方法について説明します。

## <a name="overview"></a>概要

注文詳細モジュールを使用して、注文が行われた後、注文確認の詳細を表示します。 注文の確認 ID、注文の連絡先情報、およびその他の注文の詳細 (購入された品目、支払情報、出荷方法など) が表示されます。

## <a name="order-confirmation-module-properties"></a>注文確認モジュールのプロパティ

| プロパティ名  | 値 | 説明 |
|----------------|--------|-------------|
| ヘッダー        | ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**) | 注文確認モジュールには、ヘッダーを付けることができます。 既定では、**H2** ヘッダー タグがヘッダーに使用されます。 ただし、アクセシビリティ要件を満たすようにタグを変更できます。 |
| 連絡先番号 | テキスト | 連絡先番号は、注文に関連する質問に対して発行できます。 |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>注文詳細ページで使用可能なモジュール

注文の詳細ページを作成するときに、注文明細モジュールに加えて、他の関連モジュールを追加することもできます。 次にいくつか例を挙げます。

- **推奨モジュール** - 推奨モジュールを注文詳細ページに追加して、顧客に他の製品を提案することができます。
- **マーケティング モジュール** - 注文詳細ページにマーケティング モジュールを追加して、マーケティング コンテンツを表示することができます。

## <a name="create-an-order-details-page-module"></a>注文詳細ページのモジュールの作成

1. **注文詳細のテンプレート**という名前のページ テンプレートを作成します。
1. 既定ページの**メイン**スロットで、注文詳細モジュールを追加します。
1. 注文詳細モジュールで、推奨モジュールを追加します。
1. テンプレートを保存およびプレビューします。 注文確認番号のコンテキストを必要とするため、注文詳細モジュールは表示されません。
1. テンプレートの編集を終了し、公開します。
1. 作成した注文詳細テンプレートを使用して、**注文詳細ページ**という名前のページを作成します。
1. 既定のページをページ アウトラインに追加します。
1. **ヘッダー**スロットで、ヘッダー フラグメントを追加します。
1. **フッター**スロットで、フッター フラグメントを追加します。
1. **メイン** スロットで、注文詳細モジュールを追加します。
1. 注文詳細モジュールのプロパティ ウィンドウで、見出しの**注文詳細**を追加します。
1. 注文詳細モジュールの下で、推奨モジュールを追加し、**新規**および**ベストセラー**設定を使用するように構成します。
1. ページを保存してプレビューします。
1. ページの編集を終了し、公開します。

## <a name="additional-resources"></a>追加リソース

[スタート キットの概要](starter-kit-overview.md)

[コンテナー モジュール](add-container-module.md)

[購入ボックス モジュール](add-buy-box.md)

[カート モジュール](add-cart-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[ヘッダーモジュール](author-header-module.md)

[フッター モジュール](author-footer-module.md)

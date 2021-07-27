---
title: サイト セレクター モジュール
description: このトピックでは、サイト セレクター モジュールと Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b69156ee79dbbe8cbb8f5eb5988a751f0488d8e5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357741"
---
# <a name="site-selector-module"></a>サイト セレクター モジュール

[!include [banner](includes/banner.md)]

このトピックでは、サイト セレクター モジュールと Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

市場、地域、およびロケールにまたがってサイトが異なる場合は、サイトのユーザーがサイト間を移動したり、使用する買い物サイトを選択したりするための簡単な方法が必要です。 このシナリオに対応するために、サイト選択モジュールを使用すると、ユーザーは複数のサイトにまたがって閲覧できます。

サイト選択モジュールは、サイトユーザーが参照できるサイト (市場、地域、またはロケール) のリストでコンフィギュレーションされていなければなりません。

> [!NOTE]
> この階層リンク モジュールは、Dynamics 365 Commerce の 10.0.14 リリースで入手できます。

次の図は、サイトページのヘッダーに記載されているサイト選択モジュールの例を示しています。

![サイト ページのヘッダーにおけるサイト選択モジュールの例。](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>サイト セレクター モジュールのプロパティ

| プロパティ名 | 先頭値                 | 説明 |
|---------------|-----------------------|-------------|
| ヘッダー       | テキスト                  | モジュールのヘッダー。 |
| サイト オプション  | 名前、イメージ、URL      | このプロパティでは、モジュールに含まれるサイトごとに、名前、サイトのホームページへのリンク、表示するオプションのイメージを指定します。 このイメージは、フラグ、または市場、地域、ロケールのいずれかの一部の表現にすることができます。 |

## <a name="add-a-site-selector-module-to-a-page"></a>サイト セレクター モジュールをページに追加する

サイト選択モジュールは、サイトセレクタースロットの下の [ヘッダー モジュール](author-header-module.md) に追加できます。 追加した後、モジュールのヘッダーとサイトのオプションを定義できます。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[ヘッダー モジュール](author-header-module.md)

[階層リンク モジュール](add-breadcrumb.md)

[ナビゲーション メニュー モジュール](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
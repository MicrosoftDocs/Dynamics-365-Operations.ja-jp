---
title: サイト ピッカー モジュール
description: このトピックでは、サイト ピッカー モジュールと Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 04/06/2022
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
ms.openlocfilehash: ad4d4d5f950d0631059d8f509e9e808a9106eb98
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551697"
---
# <a name="site-picker-module"></a>サイト ピッカー モジュール

[!include [banner](includes/banner.md)]

このトピックでは、サイト ピッカー モジュールと Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

市場、地域、およびロケールにまたがってサイトが異なる場合は、サイトのユーザーがサイト間を移動したり、使用する買い物サイトを選択したりするための簡単な方法が必要です。 このシナリオに対応するために、サイト ピッカー モジュールを使用すると、ユーザーは複数のサイトにまたがって閲覧できます。 サイト ピッカーは、電子コマース サイトに対して [地域検出とリダイレクト](geo-detection-redirection.md) が実装されている場合にも推奨されます。そのため、[顧客は国/地域のピッカー](country-region-picker-module.md) モジュールを使用して指定したサイトの設定を上書きできます。 

サイト ピッカー モジュールは、サイト ユーザーが参照できるサイト (市場、地域、またはロケール) のリストでコンフィギュレーションされていなければなりません。 次の図は、サイトページのヘッダーに記載されているサイト ピッカー モジュールの例を示しています。

![サイト ページのヘッダーにおけるサイト ピッカー モジュールの例。](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>サイト ピッカー モジュールのプロパティ

| プロパティ名 | 値                 | Description |
|---------------|-----------------------|-------------|
| ヘッダー       | テキスト                  | モジュールのヘッダー。 |
| サイト オプション  | 名前、イメージ、URL      | このプロパティでは、モジュールに含まれるサイトごとに、名前、サイトのホームページへのリンク、表示するオプションのイメージを指定します。 このイメージは、フラグ、または市場、地域、ロケールのいずれかの一部の表現にすることができます。 |

## <a name="add-a-site-picker-module-to-a-page"></a>サイト ピッカー モジュールをページに追加する

サイト ピッカー モジュールは、[ヘッダー モジュール](author-header-module.md)の **サイト ピッカー** スロットに追加できます。 サイト ピッカー モジュールを追加した後、モジュールのヘッダーとサイトのオプションを定義できます。 通常、ヘッダー モジュールはヘッダー フラグメントに含まれています。ヘッダー モジュールはサイトの e コマース ページ間で共有できます。 次の例では、**HeaderContainer** という名前のヘッダー フラグメントに含まれるヘッダー モジュールの **サイト ピッカー** スロットにサイト ピッカー モジュールが追加されました。

![ヘッダー フラグメントにおけるサイト ピッカー モジュールの例。](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[ヘッダーモジュール](author-header-module.md)

[階層リンク モジュール](add-breadcrumb.md)

[ナビゲーション メニュー モジュール](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

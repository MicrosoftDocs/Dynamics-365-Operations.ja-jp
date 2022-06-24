---
title: 製品をカート設定に追加を適用する
description: この記事では、「製品をカートに追加」設定と、それらを Microsoft Dynamics 365 Commerce で適用する方法について説明します。
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 336bea289b22e4f6f98077f915d7d35f2a48682d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866033"
---
# <a name="apply-add-product-to-cart-settings"></a>製品をカート設定に追加を適用する

[!include [banner](includes/banner.md)]

この記事では、**製品をカートに追加** 設定と、それらを Microsoft Dynamics 365 Commerce で適用する方法について説明します。

Dynamics 365 Commerce eコマース サイトで製品をカートに追加すると、さまざまなワークフロー がサポートされます。 たとえば、サイト ユーザーをカート ページに移動する場合があります。 または、ユーザーは現在のページに残っていますが、製品がカートに追加されたという確認の通知が表示される場合があります。

さまざまなワークフローをサポートするために、Commerce サイト ビルダーの **設定 \> 拡張機能** で **製品をカートに追加** フィールドを使用できます。 次のいずれかの設定オプションを選択して、対応するワークフローを実装します。

- **カート ページに移動** – ユーザーがカートに品目を追加すると、カート ページに移動します。
- **通知を表示** – ユーザーがカートに品目を追加すると、確認通知が届き、製品詳細ページ (PDP) で引き続き閲覧できます。
- **ミニ カートの表示** – ユーザーがカートに品目を追加すると、ミニ カートの内容が表示されます。 ユーザーは、カートに入っているすべての品目を確認し、準備が整った場合はチェックアウトを続行できます。
- **通知モジュールを使用した通知の表示** – ユーザーがカートに品目を追加すると、通知モジュールを使用して確認通知が表示されます。 この設定オプションを使用するには、通知モジュールをページ ヘッダーに追加する必要があります。
- **カート ページに移動しない** – ユーザーがカートに品目を追加しても、現在のページに残ります。

次の図は、サイト ビルダーの **製品をカートに追加** 設定オプションの例を示しています。

![サイト ビルダーで製品をカートに追加設定オプションの例](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - **製品をカートに追加** サイト設定は、Dynamics 365 Commerce バージョン 10.0.11 リリースから使用できます。 古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。 appsettings.json ファイルを更新する方法の詳細については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) を参照してください 。
> - **ミニ カートの表示** 設定オプションは、Dynamics 365 Commerce バージョン 10.0.20 リリースから使用できます。 古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。 appsettings.json ファイルを更新する方法の詳細については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) を参照してください 。

次の図では、Fabrikam サイトにおいて "カートに追加された" 際の確認通知の例を示しています。

![Fabrikam サイトにおいて "カートに追加された" 際の確認通知の例](./media/ecommerce-addtocart-notifications.PNG)

次の図では、Adventure Works サイトにおいて "カートに追加された" 際の確認通知の例を示しています。

![Adventure Works サイトにおいて "カートに追加された" 際の確認通知の例](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[購入ボックス モジュール](add-buy-box.md)

[店舗セレクター モジュール](store-selector.md)

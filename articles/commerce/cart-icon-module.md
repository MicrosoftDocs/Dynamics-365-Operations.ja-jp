---
title: 買い物カゴ アイコン モジュール
description: このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661150"
---
# <a name="cart-icon-module"></a>買い物カゴ アイコン モジュール

[!include [banner](includes/banner.md)]

このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

## <a name="overview"></a>概要

買い物カゴ アイコン モジュールは、ページのヘッダー モジュールで買い物カゴを表し、買い物カゴ内の品目数を示します。 買い物カゴ アイコン モジュールには、買い物カゴ アイコンにカーソルを合わせると、買い物カゴの概要 (ミニカートとも呼ばれる) も表示されます。 ミニ カートには、買い物カゴ ページに移動することなく、買い物カゴ内の品目の概要が表示されます。 また、ユーザーが概要に満足している場合、チェックアウト ページに直接移動することもできます。 これにより、ページ ナビゲーションの回数が減り、迅速にチェックアウトできるようになります。 

次の図は、Fabrikam のヘッダーでミニ買い物カゴを表示する買い物カゴのアイコン モジュールの例を示しています。

![買い物カゴ アイコン モジュールの例](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>モジュール プロパティ

- **ミニ カートの表示** – True の場合、このプロパティにより、買い物カゴ アイコンにカーソルを合わせると買い物カゴの概要 (ミニ カート) が表示されます。 この機能は、デスクトップ 表示ポートに対してのみサポートされています。

## <a name="add-a-cart-icon-module-to-a-page"></a>買い物カゴ アイコン モジュールをページに追加する

買い物カゴ アイコン モジュールを追加するには、[ヘッダー モジュール](author-header-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[買い物カゴ モジュール](add-cart-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[支払モジュール](payment-module.md)

[出荷先住所モジュール](ship-address-module.md)

[配送オプション モジュール](delivery-options-module.md)

[注文詳細のモジュール](order-confirmation-module.md)

[ギフト カード モジュール](add-giftcard.md)

---
title: 買い物カゴ アイコン モジュール
description: このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
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
ms.openlocfilehash: e0238e9d464fc1d44cbc5091638ac7270d5b6ae3
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479307"
---
# <a name="cart-icon-module"></a>カート アイコン モジュール

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

買い物カゴ アイコン モジュールは、ページのヘッダー モジュールで買い物カゴを表し、買い物カゴ内の品目数を示します。 買い物カゴ アイコン モジュールには、買い物カゴ アイコンにカーソルを合わせると、買い物カゴの概要 (ミニカートとも呼ばれる) も表示されます。 ミニ カートには、買い物カゴ ページに移動することなく、買い物カゴ内の品目の概要が表示されます。 また、ユーザーが概要に満足している場合、チェックアウト ページに直接移動することもできます。 これにより、ページ ナビゲーションの回数が減り、迅速にチェックアウトできるようになります。 

次の図は、Fabrikam のヘッダーでミニ買い物カゴを表示する買い物カゴのアイコン モジュールの例を示しています。

![買い物カゴ アイコン モジュールの例。](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>モジュール プロパティ

- **ミニ カートの表示** – True の場合、このプロパティにより、買い物カゴ アイコンにカーソルを合わせると買い物カゴの概要 (ミニ カート) が表示されます。 この機能は、デスクトップ 表示ポートに対してのみサポートされています。

## <a name="module-properties-in-the-adventure-works-theme"></a>Adventure Works テーマのモジュール プロパティ

Adventure Works のテーマでは、買い物カゴ アイコン モジュールには、ミニ カートに対する 2 つの追加スロットが含まれています。 これらのスロットは、モジュール定義拡張機能として含まれます。

- **空の買い物カゴ プロモーション** – このスロットでは、コンテンツ ブロック モジュールが使用されます。 買い物カゴが空の場合は、指定したコンテンツ ブロック モジュールが表示されます。 コンテンツ ブロック モジュールは、プロモーション、マーケティング コンテンツ、およびカテゴリ ページへのリンクに使用され、顧客が買い物を促進し続けるのに役立ちます。
- **プロモーション コンテンツ** – このスロットは、「100 ドル以上のご注文で送料無料」などのプロモーションを紹介するために使用できます。 コンテンツ ブロック、テキスト ブロック、およびイメージ リスト モジュールは、プロモーション コンテンツ スロットで使用されます。

次の図は、ミニ カートにプロモーション コンテンツを表示する Adventure Works テーマの買い物カゴ アイコン モジュールの例を示します。

![Adventure Works テーマのカ買い物カゴ アイコン モジュールの例](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Adventure Works テーマ スロットは、Dynamics 365 Commerce バージョン 10.0.20 リリース時点で使用できます。

## <a name="add-a-cart-icon-module-to-a-page"></a>買い物カゴ アイコン モジュールをページに追加する

買い物カゴ アイコン モジュールを追加するには、[ヘッダー モジュール](author-header-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[買い物カゴ モジュール](add-cart-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[支払モジュール](payment-module.md)

[出荷先住所モジュール](ship-address-module.md)

[配送オプション モジュール](delivery-options-module.md)

[集荷情報モジュール](pickup-info-module.md)

[注文詳細のモジュール](order-confirmation-module.md)

[ギフト カード モジュール](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

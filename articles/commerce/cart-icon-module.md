---
title: 買い物カゴ アイコン モジュール
description: このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 08/02/2021
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
ms.openlocfilehash: 5cf86876ba03d510b03237c9c89a1fc069a73482b755a1d72227037c91439e86
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735681"
---
# <a name="cart-icon-module"></a>カート アイコン モジュール

[!include [banner](includes/banner.md)]

このトピックでは、買い物カゴ アイコン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

買い物カゴ アイコン モジュールは、ページのヘッダー モジュールで買い物カゴを表し、買い物カゴ内の品目数を示します。 買い物カゴ アイコン モジュールには、買い物カゴ アイコンにカーソルを合わせると、買い物カゴの概要 (ミニカートとも呼ばれる) も表示されます。 ミニ カートには、買い物カゴ ページに移動することなく、買い物カゴ内の品目の概要が表示されます。 また、ユーザーが概要に満足している場合、チェックアウト ページに直接移動することもできます。 これにより、ページ ナビゲーションの回数が減り、迅速にチェックアウトできるようになります。 

次の図は、Fabrikam のヘッダーでミニ買い物カゴを表示する買い物カゴのアイコン モジュールの例を示しています。

![買い物カゴ アイコン モジュールの例。](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>モジュール プロパティ

- **ミニカートを表示** – このプロパティが **True** に設定されている場合、ユーザーがカート アイコンにカーソルを合わせると、カートの概要 (ミニカート) が表示されます。 この機能は、デスクトップ表示ポートに対してのみサポートされています。
- **匿名チェックアウトを許可する** – このプロパティが **True** に設定されている場合、ミニカートはサインインしていないユーザーがゲスト チェックアウトを実行できるようにします。 このプロパティは、Commerce モジュール ライブラリ パッケージの一部として、Commerce バージョン 10.0.21 リリースで使用できます。
- **項目の順序** : このプロパティは、ミニカートにアイテムが表示される順序を制御します。 **リストの一番上に追加された新しいアイテム** オプションを選択すると、カートに追加された新しいアイテムがミニカート アイテムのリストの一番上に表示されます。 既定のオプションである **リストの一番下に追加された新しいアイテム** を選択すると、カートに追加された新しいアイテムがミニカート アイテムのリストの一番下に表示されます。 このプロパティは、Commerce モジュール ライブラリ パッケージの一部として、Commerce バージョン 10.0.21 リリースの時点で使用できます。

> [!IMPORTANT]
> **匿名チェックアウトを許可** し、**項目の順序** プロパティが Commerce バージョン 10.0.21 のリリースで使用可能です。 Commerce モジュール ライブラリ パッケージのバージョン 9.31 がインストールされている必要があります。

## <a name="module-properties-and-slots-in-the-adventure-works-theme"></a>Adventure Works テーマのモジュール プロパティとスロット

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

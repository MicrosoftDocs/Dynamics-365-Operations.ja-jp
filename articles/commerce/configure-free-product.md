---
title: 無料で購入できる製品を構成する
description: この記事では、Microsoft Dynamics 365 Commerce で無料で購入できるように製品を構成する方法について説明します。
author: anupamar-ms
ms.date: 10/27/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bd7e4f7a7873e471f1aee94f15e7932e8d9eecd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890358"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>無料で購入できる製品を構成する

[!include [banner](includes/banner.md)]


この記事では、Microsoft Dynamics 365 Commerce で無料で購入できるように製品を構成する方法について説明します。

## <a name="configure-the-product"></a>製品を構成する

製品を Dynamics 365 Commerce で自由に販売するには、その価格を 0 (ゼロ) に設定する必要があります。 また、製品の **ゼロ価格の有効** 設定を構成する必要があります。

Commerce 本社で **ゼロ価格の有効** 設定を構成するには、次の手順に従います。

1. **Retail と Commerce \> 製品とカテゴリ \> カテゴリ別リリース済製品** の順に移動します。
1. 無料で販売する製品に移動します。 
1. 製品ページの **Commerce** セクションで、**ゼロ価格の有効** オプションを **はい** に設定 します。

次の図は、**ゼロ価格の有効** オプションが **はい** に設定されている製品の例を示しています。

![[ゼロ価格の有効] オプションが [はい] に設定されている製品の例。](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>オンラインストアの機能プロファイルを構成する

無料の取引を処理する前に、オンラインストアの機能プロファイルの **支払いのないチェックアウトを許可する** 設定を構成して、支払いのない取引を許可するように設定する必要があります。 機能プロファイルの作成方法の詳細については、[オンライン機能プロファイルの作成](online-functionality-profile.md)を参照してください。

Commerce 本社で **支払いのないチェックアウトを許可する** 設定を構成するには、次の手順に従います。

1. **Retail と Commerce \>  チャネル設定 \> オンライン ストアの設定**  機能プロファイルの順に移動します。
1. ストアの機能プロファイルのページの **チェックアウト** で、**支払いのないチェックアウトを許可する** オプションを **はい** に設定します。

次の図は、**支払いのないチェックアウトを許可する** オプションが **はい** に設定されているオンライン ストアのプロファイルの例です。

![支払いのないチェックアウトを許可するオプションがはいに設定されているオンライン ストアのプロファイルの例。](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>追加リソース

[小売販売価格の管理](price-management.md)

[オンライン機能プロファイルの作成](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

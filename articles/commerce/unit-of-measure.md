---
title: 測定単位設定の適用
description: このトピックでは測定単位設定を取り上げ、Microsoft Dynamics 365 Commerce で適用する方法について説明します。
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022377"
---
# <a name="apply-unit-of-measure-settings"></a>測定単位設定の適用

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは測定単位設定を取り上げ、Microsoft Dynamics 365 Commerce で適用する方法について説明します。

製品は、「各」、「ペア」、「ダース」など、異なる単位で販売できます。 Commerce 本社では、測定単位の販売は製品を定義して、eコマース サイトに表示できます。 たとえば、小売業者が個別と数十単位の両方で製品を販売する場合、使用可能な測定単位を他の製品情報と共に表示できます。

次の図の例では、**ea** (それぞれ) の測定単位の販売は、Commerce 本部の製品用に構成されています。

![Commerce 本部の測定単位で構成されている製品の例](./media/Productunit-headquarters.PNG)

> [!NOTE]
> 測定単位の適用および表示のサポートは、Commerce のバージョン 10.0.19 リリース以降で利用できます。

## <a name="unit-of-measure-settings"></a>測定単位設定

測定単位の表示設定は、Commerce サイト ビルダーの、**サイト設定 \> 拡張機能 \> 製品の測定単位の表示** で定義されます。 サポートされている設定は 3 つあります。

- **表示しない** – この設定が選択されている場合、eコマース サイトに製品の測定単位は表示されません。 この動作は既定の動作です。
- **製品の購入経験での表示**: この設定が選択されている場合、測定単位は製品の詳細、カート、チェックアウト、注文履歴、および注文の詳細ページに表示されます。
- **製品閲覧および購入エクスペリエンスでの表示**: この設定が選択されている場合、測定単位は製品の購入エクスペリエンスページおよび製品ブラウジングエクスペリエンス中にも表示されます。 この動作の一部として、測定単位は、検索結果および製品収集モジュールに表示されます。

> [!IMPORTANT]
> 測定単位の表示設定は、Commerce のバージョン 10.0.19 リリース以降で使用できます。 古いバージョンの Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。 手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) を参照してください。

## <a name="modules-that-use-unit-of-measure-settings"></a>測定単位の設定を使用するモジュール

測定単位の設定を使用するモジュールには、購入ボックス、欲しい物リスト、買い物カゴ、買い物カゴ アイコン、検索結果コンテナー、製品コレクション、チェックアウト、注文詳細モジュールが含まれます。

次の図の例では、製品の詳細ページ (PDP) は、製品の測定単位 (**ea**) を示しています。

![測定単位を示す PDP の例](./media/Productunit-PDP.png)

次の図の例では、製品収集モジュールは、製品の測定単位 (**ea**) を示しています。

![測定単位を示す製品収集モジュールの例](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[カート モジュール](add-cart-module.md)

[購入ボックス モジュール](add-buy-box.md)

[アカウント管理ページとモジュール](account-management.md)

[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

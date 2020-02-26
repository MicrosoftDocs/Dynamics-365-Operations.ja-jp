---
title: 販売促進エンティティの並べ替え順序の変更
description: このトピックでは、Dynamics 365 Commerce で、販売促進に関連したさまざまなエンティティに対する表示順序の制御に関連する概念について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b983cb5c63db171c76d34375a93a2b9086185d3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023129"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>販売促進エンティティの並べ替え順序の変更


[!include [banner](includes/banner.md)]

小売業者は、製品の検出を、すべてのチャネルでの顧客とのやり取りにおける主要なツールと考えています。 さまざまな機能により、顧客が製品を簡単に検索できるようになります。 たとえば、カテゴリ、検索、およびフィルターを参照できます。

このトピックでは、 販売促進に関連したさまざまなエンティティに対する表示順序の制御に関連する概念について説明します。 また、並べ替え順序を変更する方法についても説明します。

## <a name="overview"></a>概要

販売促進に関連したさまざまなエンティティを並べ替えるためのサポートが強化されました。 このサポートにより、以前には実装パートナーからの拡張を必要としていた既存の顧客シナリオとの整合性が向上しました。

バージョン 10.0.5 よりも前の Retail のバージョンでは、ナビゲーション階層でのカテゴリの並べ替え順序はアルファベット順になっていました。 新しいカスタム並べ替え順序機能を使用すると、販売促進マネージャーは、すべてのエンド ユーザー クライアントでの販売促進に関連したさまざまなエンティティの並べ替え順序をコンフィギュレーションできます。 これらのクライアントには、本社 (HQ) およびコール センターが含まれます。

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>製品階層でのカテゴリに対する表示順序のコンフィギュレーション

この手順を完了する前に、デモ データが環境にインストールされている必要があります。

1. **Retail と Commerce \> 製品とカテゴリ \> Commerce 製品階層**に移動します。
2. **カテゴリ階層の編集**をクリックします。
3. **編集** をクリックします。
4. ツリーで、**ALL \> Action Sports** を展開します。
5. ツリーで、**ALL \> Team Sports** を展開します。
6. **表示順序**フィールドに数値を入力します。 (数値は負の場合があります。)
7. 順序を変更する追加のカテゴリに対して、手順 4 ～ 6 を繰り返します。

チャネル ナビゲーション階層の表示順序は、Commerce 製品階層およびカテゴリ別のリリース済製品に対して HQ で反映されます。

![負の値でカスタム並べ替えされた製品階層](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![製品階層に基づいてカスタム並べ替えされた、カテゴリ別のリリース済製品](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>チャネル ナビゲーション階層でのカテゴリに対する表示順序のコンフィギュレーション

この手順を完了する前に、デモ データが環境にインストールされている必要があります。

1. **Retail と Commerce \> 製品とカテゴリ \> チャネル ナビゲーション カテゴリ**の順に移動します。
2. 一覧で、**ファッション ナビゲーション**階層を選択します。
3. **カテゴリ階層の編集**をクリックします。
4. **編集** をクリックします。
5. ツリーで、**ファッション \> ウィメンズウェア \> ウィメンズ シューズ** を選択します。
6. **表示順序**フィールドに数値を入力します。
7. ツリーで、**ファッション \> ウィメンズウェア \> トップス** を選択します。

    同様に、サブカテゴリの並べ替え順序を定義できます。

8. ツリーで、**ファッション \> メンズウェア \> カジュアル シャツ** を選択します。
9. **表示順序**フィールドに数値を入力します。
10. ツリーで、**ファッション \> メンズウェア \> コート & ジャケット** を選択します。
11. **表示順序**フィールドに数値を入力します。
12. 順序を変更する任意の追加のカテゴリに対して繰り返します。

チャネル ナビゲーション階層の表示順序は HQ、カタログ、およびチャネルで反映されます。

![カスタム並べ替えされたチャネル ナビゲーション階層](./media/ChannelNavCustomSorted.png)

![チャネル ナビゲーション階層に基づいてカスタム並べ替えされた、カタログ ナビゲーション階層](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![カスタム並べ替えされたカテゴリを含む POS](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> 既定では、カスタム並べ替え順序機能が無効になっています。 この機能およびその他の機能を有効にする方法については、[機能管理](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview) を参照してください。

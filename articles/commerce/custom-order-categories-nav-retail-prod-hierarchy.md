---
title: 販売促進エンティティの並べ替え順序の変更
description: この記事では、Dynamics 365 Commerce で、販売促進に関連したさまざまなエンティティに対する表示順序の制御に関連する概念について説明します。
author: josaw1
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265839"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>販売促進エンティティの並べ替え順序の変更


[!Include [banner](includes/banner.md)]

小売業者は、製品の検出を、すべてのチャネルでの顧客とのやり取りにおける主要なツールと考えています。 顧客が製品を簡単に見つけるのに役立つ機能がいくつかあります。 たとえば、顧客は、カテゴリ、検索、およびフィルターを参照できます。

この記事では、販売促進に関連したさまざまなエンティティに対する表示順序の制御に関連する概念について説明します。 また、並べ替え順序を変更する方法についても説明します。

## <a name="overview"></a>開始する

Commerce では、さまざまな販売促進に関連するエンティティの並べ替えは、既存の顧客シナリオに沿ったものであり、実装パートナーからの拡張機能は不要になります。

Commerce バージョン 10.0.5 およびそれ以前では、ナビゲーション階層でのカテゴリの並べ替え順序はアルファベット順でした。 現在のカスタム並べ替え順序機能を使用すると、販売促進マネージャーは、すべてのエンド ユーザー クライアントでの販売促進に関連したさまざまなエンティティの並べ替え順序を構成できます。 これらのクライアントには、本社 (HQ) およびコール センターが含まれます。

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>製品階層でのカテゴリに対する表示順序のコンフィギュレーション

この手順を完了する前に、デモ データが環境にインストールされている必要があります。

1. **Retail と Commerce \> 製品とカテゴリ \> Commerce 製品階層** に移動します。
2. **カテゴリ階層の編集** をクリックします。
3. **編集** をクリックします。
4. ツリーで、**ALL \> Action Sports** を展開します。
5. ツリーで、**ALL \> Team Sports** を展開します。
6. **表示順序** フィールドに数値を入力します。 (数値は負の場合があります。)
7. 順序を変更する追加のカテゴリに対して、手順 4 ～ 6 を繰り返します。

チャネル ナビゲーション階層の表示順序は、Commerce 製品階層およびカテゴリ別のリリース済製品に対して HQ で反映されます。

![負の値でカスタム並べ替えされた製品階層。](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![製品階層に基づいてカスタム並べ替えされた、カテゴリ別のリリース済製品。](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>チャネル ナビゲーション階層でのカテゴリに対する表示順序のコンフィギュレーション

この手順を完了する前に、デモ データが環境にインストールされている必要があります。

1. **Retail と Commerce \> 製品とカテゴリ \> チャネル ナビゲーション カテゴリ** の順に移動します。
2. 一覧で、**ファッション ナビゲーション** 階層を選択します。
3. **カテゴリ階層の編集** をクリックします。
4. **編集** をクリックします。
5. ツリーで、**ファッション \> ウィメンズウェア \> ウィメンズ シューズ** を選択します。
6. **表示順序** フィールドに数値を入力します。
7. ツリーで、**ファッション \> ウィメンズウェア \> トップス** を選択します。

同様に、サブカテゴリの並べ替え順序を定義できます。

8. ツリーで、**ファッション \> メンズウェア \> カジュアル シャツ** を選択します。
9. **表示順序** フィールドに数値を入力します。
10. ツリーで、**ファッション \> メンズウェア \> コート & ジャケット** を選択します。
11. **表示順序** フィールドに数値を入力します。
12. 順序を変更する任意の追加のカテゴリに対して繰り返します。

チャネル ナビゲーション階層の表示順序は HQ、カタログ、およびチャネルで反映されます。

![カスタム並べ替えされたチャネル ナビゲーション階層。](./media/ChannelNavCustomSorted.png)

![チャネル ナビゲーション階層に基づいてカスタム並べ替えされた、カタログ ナビゲーション階層。](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![カスタム並べ替えされたカテゴリを含む POS。](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> 既定では、**販売促進エンティティの表示順序の有効化** 機能は無効になっています。 [機能管理](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して有効にします。 機能を有効にした後、配送スケジュールから **グローバル構成 -1110** CDX ジョブを実行します。
> POS でカテゴリの順序が更新されない場合は、デバイスを再度有効にします。 カテゴリ情報は、デバイスのアクティブ化が発生したときにフェッチされるため、デバイスは更新された表示順序でカテゴリ情報の再フェッチが必要な場合があります。 

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: チャンネル固有の割引の定義
description: 小売業者は、多くの場合、異なるチャンネルのさまざまな割引を設定します。 この記事では、特定のチャンネルの割引を作成するために知っておく必要のある概念を確認します。
author: scott-tucker
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9ceb5c8e47288e7ffdd3808cd8d60112f81ce314
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873413"
---
# <a name="define-channel-specific-discounts"></a>チャネル固有の割引の定義

[!include [banner](includes/banner.md)]

この記事では、特定のチャンネルの割引を作成するために知っておく必要のある概念を確認します。

## <a name="channel-specific-discounts"></a>チャンネル固有の割引

小売業者は、多くの場合、異なるチャンネルでさまざまな割引を提供します。 それらは、国内市場の状況に合わせて行われたり、競合の小売業者に対処するために行われる場合があります。

Commerce は、チャネル固有の割引を定義するために価格グループを使用します。 価格グループは、次のエンティティーの 1 つ以上に割り当てることができます: チャンネル、カタログ、加盟者、ロイヤルティー プログラム。 この記事ではチャンネルについて説明しますが、カタログ割引、加盟者割引、ロイヤルティー割引に対しても同じ概念が適用できます。

## <a name="price-groups"></a>価格グループ

[![価格グループ。](./media/price-groups-1024x608.png)](./media/price-groups.png)

上記の図は、トランザクションで扱うことができるエンティティ (チャンネル、カタログ、加盟者、顧客、ロイヤルティ カード) とさまざまな設定可能な割引との間の関係を説明しています。 すべてのトランザクションはチャンネルで発生するため、あるトランザクションに対してチャンネルが存在することが保証されます。 残りのエンティティーはオプションです。 各マスター データ ページには、関連する価格グループのページへのリンクがあり、必要に応じて価格グループを表示および追加できます。 価格グループを使用すると、4 つの異なるエンティティ タイプを、割引、価格調整、売買契約に関連付けることができます。 価格グループの名前の付け方を戦略的に計画し、整理しておくことをお勧めします。 1 つの案は、文字または数字の接頭語や接尾辞を使用して、タイプを区別することです。 たとえば、1-xxxxx をチャンネルの価格グループに、2-xxxxx をカタログの価格グループに割り当てます。 4 つの照会ページが提供され、関連付いた割引がある可能性のある Commerce エンティティーをそれぞれ表示します。

- **チャネル チャネルの価格グループ** – このページには、それぞれの価格グループにリンクされているチャンネルと割引の一覧が表示されます。
- **カタログの価格グループ** ー このページには、それぞれの価格グループにリンクされているカタログと割引の一覧が表示されます。
- **ロイヤルティーの価格グループ** ー このページには、それぞれの価格グループにリンクされているロイヤルティー プログラムと割引の一覧が表示されます。
- **加盟者の価格グループ** ー このページには、それぞれの価格グループにリンクされている加盟者と割引の一覧が表示されます。

## <a name="example-channel-discount-set-up"></a>チャンネルの割引設定の例

次の例は、チャンネル割引の設定に関連するタスクについて説明したものです。

1. この例では、**ヒューストン** というチャネルがあり、新しい割引 **新学期** を作成しようとしています。
2. 価格と割引の戦略にはチャンネル割引が含まれる可能性があるため、チャンネル作成時には常に特定チャンネルの価格グループを作成します。
3. **ヒューストンPG** という価格グループがあり、チャンネル **ヒューストン** に割り当てられています。
4. 新しい割引 **新学期** を作成した後、**割引** ページの上部にある **価格グループ** をクリックします。 **割引価格グループ** ページが表示されます。 次に、**新規** をクリックして、価格グループ **ヒューストンPG** を選択します。
5. これで、割引を有効にして、チャンネルにプッシュすることができます。

## <a name="additional-resources"></a>その他のリソース

[価格調整と割引](price-adjustments-discounts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: "チャンネル固有の割引の定義"
description: "小売業者は、多くの場合、異なるチャンネルのさまざまな割引を設定します。 このトピックでは、特定のチャンネルの割引を作成するために知っておく必要のある概念を確認します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>チャンネル固有の割引の定義

小売業者は、多くの場合、異なるチャンネルのさまざまな割引を設定します。 このトピックでは、特定のチャンネルの割引を作成するために知っておく必要のある概念を確認します。 

<a name="channel-specific-discounts"></a>チャンネル固有の割引
--------------------------

小売業者は、多くの場合、異なるチャンネルのさまざまな割引が提供されます。 これはかもしされることがあります市況ローカルに対処するか、または競合の小売業者に対処するためにあります。

、Microsoft Dynamics 365 for Operationsの[小売りとコマースは、チャンネル固有の割引を定義する、価格グループを使用します。 価格グループは、次のエンティティーの 1 つ以上に割り当てることができます: チャンネル、カタログ、加盟者、ロイヤルティー プログラム。 この記事ではチャンネルについて説明しますが、カタログ割引、加盟者割引、ロイヤルティー割引に対しても同じ概念が適用できます。

## <a name="price-groups"></a>価格グループ
\[キャプションid=の添付ファイル"\_"256084 align=の" alignnone」width= "640 "\][![価格グループ] (。/media/priceグループ1024x608.png) ] (。/media/price-groups.png) 価格グループを小売]\[/caption\]にリンクされます

前の図は、コンフィギュレーションする各種割引タイプとトランザクション (チャンネル、カタログ、所属、顧客、ロイヤルティ カード) であるエンティティ間の関係を説明します。 すべてのトランザクションは、チャンネルに発生します。したがって、チャンネルは、トランザクションである場合に支払保証されます。 残りのエンティティーはオプションです。 各マスター データ ページには、関連する価格グループのページへのリンクがあり、必要に応じて価格グループを表示および追加できます。 価格グループが割引、価格調整および売買契約のエンティティの4つのタイプを関連付ける目的で使用されます。 ただし、価格グループをいる組織を保持するにどのように名前を付けるや戦略を計画することをお勧めします。 一つのオプションは、文字を使用するか、またはさまざまなタイプを区別する市外局番または接尾語の番号付け。 たとえば、チャンネルの価格グループの1-xxxxxおよびカタログの価格グループの2-xxxxx。 4 つの照会ページが提供され、関連付いた割引がある可能性のある小売エンティティーをそれぞれ表示します。

-   **小売チャンネルの価格グループ** - このページには、それぞれの価格グループにリンクされているチャンネルと割引の一覧が表示されます。
-   **カタログの価格グループ** - このページには、それぞれの価格グループにリンクされているカタログと割引の一覧が表示されます。
-   **ロイヤルティーの価格グループ** - このページには、それぞれの価格グループにリンクされているロイヤルティー プログラムと割引の一覧が表示されます。
-   **加盟者の価格グループ** - このページには、それぞれの価格グループにリンクされている加盟者と割引の一覧が表示されます。

## <a name="example-channel-discount-set-up"></a>チャンネルの割引設定の例
次の例は、チャンネル割引の設定に関連するタスクについて説明したものです。

1.  この例では、**ヒューストン**というチャンネルがあり、新しい割引**新学期**を作成しようとしています。
2.  価格と割引の戦略にはチャンネル割引が含まれる可能性があるため、チャンネル作成時には常に特定チャンネルの価格グループを作成します。
3.  **ヒューストンPG**という価格グループがあり、チャンネル**ヒューストン**に割り当てられています。
4.  新しい割引**新学期**を作成した後、**割引**ページの上部にある**価格グループ**をクリックします。 **割引価格グループ**ページが表示されます。 次に、**新規**をクリックして、価格グループ**ヒューストンPG**を選択します。
5.  これで、割引を有効にして、チャンネルにプッシュすることができます。

 

<a name="see-also"></a>参照
--------

[Price adjustments and discounts](price-adjustments-discounts.md)



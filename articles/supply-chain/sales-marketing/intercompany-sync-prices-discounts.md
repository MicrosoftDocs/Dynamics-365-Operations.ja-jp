---
title: 会社間の価格と割引の同期
description: この記事では、会社間の販売注文書と会社間発注書に対する価格と割引の同期について説明します
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 64130c400212a819f931cc36459667e4d7c83f32
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905692"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>会社間の価格と割引の同期

[!include [banner](../../includes/banner.md)]

割引と価格は、会社間販売注文書と会社間発注書の間で常に同期されます。 すべての注文の価格と割引が同じになるように、価格と割引を元の販売注文との間でも同期させることができます。 これは、**すべての顧客** リスト ページの **全般** タブからアクセスする **会社間** ページ (**販売とマーケティング** または **調達**) から行います。

**価格と割引** フィールドは、会社間販売注文明細行に同期されます。 つまり、**価格編集を許可** フィールドと **割引編集を許可** フィールドを選択することで、会社間販売注文書と会社間発注書の間で変更を許可したことになります。 会社間販売注文書で単価、価格単位、または販売手数料を変更すると、会社間発注書の明細行の価格が決まります。

会社間販売注文書または会社間発注書で **価格編集を許可** フィールドと **割引編集を許可** フィールドが有効になっている場合、いずれかの注文書で価格または割引を手動で変更できます。 それ以外の場合はできません。

会社間販売注文書で **価格編集を許可** フィールドと **割引編集を許可** フィールドが有効になっていない場合、会社間販売注文書で価格 (または諸費用) または割引を手動で変更することはできません。

会社間発注書で **価格編集を許可** フィールドと **割引編集を許可** フィールドが有効になっていない場合、会社間発注書で価格 (または諸費用) または割引を手動で変更することはできません。

会社間発注書と会社間販売注文書の両方で **価格編集を許可** フィールドと **割引編集を許可** フィールドが有効になっている場合、両方の注文書を手動で変更できます。 ただし、ある担当者が行った更新が、別会社の別の担当者が行った同じ注文に対する更新によって取り消される状況が発生する可能性があります。

> [!NOTE]
> 会社間発注書と会社間販売注文書の両方で **価格と割引** フィールドを有効にした場合は、価格設定を制御できなくなります。

このような競合を回避するためには、価格と割引の変更を会社間販売注文書または会社間発注書でのみ許可することをお勧めします。 これは、これらの注文書のいずれかで **価格編集を許可** フィールドと **価格編集を許可** フィールドを有効にすることで実行されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

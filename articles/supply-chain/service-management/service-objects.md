---
title: サービス対象の概要
description: この記事では、サービス対象の使用方法について説明します。
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8150a94677fe38f4caa6f3e0b5fb5d1be5972eaf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862414"
---
# <a name="service-objects-overview"></a>サービス対象の概要

[!include [banner](../includes/banner.md)]

サービス対象とは、サービスを実行する顧客の製品および資産です。 提供するサービスのタイプに応じて、有形または無形の対象を使用できます。

-  有形の対象は、機械や建物などの物です。有形の対象では、物理的なサービス作業を実行できます。

    有形のサービス対象はさらに、[リリース済製品の詳細] フォームで作成する在庫品目にすることもできます。 品目に関連付ける在庫分析コード グループに応じて、品目シリアル番号を含む詳細のレベルへのサービス対象を作成することができます。 これは、サービス対象が表す正確な品目を追跡する必要がある場合に役立ちます。

    有形のサービス対象はさらに、会社の直接生産またはサプライ チェーンに直接関係しない品目とすることもできます。 たとえば、サービス注文の修復に使用されるツールキットは棚卸資産に含まれていないサービス対象とすることができます。 この場合、在庫品目として登録されません。

-  無形の対象は、勘定のセットや法的文書などの非物質的なもので、サービス作業は、これらの無形の対象に基づいて実行できます。

## <a name="example-of-an-intangible-service-object"></a>無形のサービス対象の例

会社 A は複数の小規模な会社の財務レコードを管理します。 会社 A の顧客の 1 つはローカル フットボール チームで、それに対して、会社 A はクラブの口座の週次簿記および年次監査を行います。 クラブの口座は [サービス対象] フォームで設定され、対象としてサービス契約で指定されます。 対象には 2 つのサービス契約明細行があります。 行 1 は明細行に割り当てられている週次間隔の週次簿記で、行 2 はそれに割り当てられている年次間隔の年次監査です。

## <a name="related-articles"></a>関連記事

[サービス対象の作成](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
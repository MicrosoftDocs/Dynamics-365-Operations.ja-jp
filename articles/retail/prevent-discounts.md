---
title: 小売製品の割引を禁止するためのオプション
description: 小売業者はさまざまな理由で、一部の製品の割引を、プロモーションからまたは POS での販売中に禁止します。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 64f54c1a63706ccd9225d47df96ffc3f88cf3332
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606921"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>小売製品の割引を禁止するためのオプション

[!include [banner](includes/banner.md)]

小売業者はさまざまな理由で、一部の製品の割引を、プロモーションからまたは POS での販売中に禁止します。

リリース済製品の**小売**タブ上で表示される次のオプションで、すべてのまたは手動の割引を禁止するよう製品をコンフィギュレーションできます。 その設定は、小売カテゴリ階層からカテゴリ レベルで指定することもできます。

- **すべての割引を禁止** – すべてのタイプの割引をこの製品に適用禁止にするには、このオプションを選択します。 これには、組み合わせ、数量およびしきい値割引などのプロモーション、また POS ユーザーによる販売中に適用される手動の明細行およびトランザクションの割引が含まれます。
- **手動の割引を禁止** – POS ユーザーによる販売中に適用される手動の明細行またはトランザクションの割引のみを禁止するには、このオプションを選択します。 このオプションを選択した製品は、組み合わせ、数量およびしきい値割引などのプロモーションについてはまだ対象となっています。

> [!NOTE]
> 価格上書き操作は、基準価格の設定をするもので割引としては扱われないので、これらの設定によって制限されません。

[![割引フィールドの禁止](./media/prevent-discounts.png)](./media/prevent-discounts.png)

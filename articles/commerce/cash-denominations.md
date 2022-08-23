---
title: 販売時点管理 (POS) 用の現金貨幣単位のコンフィギュレーション
description: 紙幣および硬貨の現金貨幣単位は、POS 内で店舗のレジ担当者、店員およびマネージャーにより使用されるバック オフィスで定義できます。
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.industry: Retail
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
ms.openlocfilehash: c61cde76bf2bfe3ff48b306a8a161fa27f50ac41
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273696"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>販売時点管理 (POS) 用の現金貨幣単位のコンフィギュレーション

[!include [banner](includes/banner.md)]

紙幣および硬貨の現金貨幣単位は、POS 内で店舗のレジ担当者、店員およびマネージャーにより使用されるバック オフィスで定義できます。 これらの貨幣単位は、営業終了時の支払/入金申告、または売上の簡単な支払/入金の現金計算をする助けとして使用できます。

## <a name="define-denominations"></a>貨幣単位の定義

貨幣単位は店舗ごとに、店舗のプロパティ ページから **設定** \> **現金申告** オプションで設定されます。

![現金申告オプション。](./media/image1-denomination.png)

貨幣単位を定義する方法:

1. **新規** をクリックします。
1. 種類 (硬貨または紙幣) を指定します。
1. 金額 (値) を指定します。

![現金申告貨幣ページ。](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>機能プロファイルのコンフィギュレーション

POS での現金による支払の際、ユーザーは、顧客によって支払われた金額をすばやく入力するため紙幣の通貨単位を使用できます。 機能プロファイルで、POSで貨幣単位を表示するための 2 つのオプションをコンフィギュレーションできます。

- **合計金額以上** ー 既定では、POS は未払い金額より多い紙幣の通貨単位のみを表示し、ワンタッチの支払/入金ができるようにします。 たとえば、請求額が $7.50 の場合、POS は次の通貨単位を表示します: $10、$20、$50、および $100。 これらの金額のいずれかにタッチすると、自動的にその金額に対する売上の支払/入金をします。 $1 および $5 紙幣、これらの金額は、請求額よりも少ないため表示されません。
- **すべての貨幣単位** ー 請求額に関係なく、POS で常にすべての紙幣の貨幣単位を表示するために、このオプションを選択します。 つまり、ユーザーは請求額に達する紙幣の組み合わせを使用できます。 たとえば、請求額が $25.00 の場合は、ユーザーは $20 よび $5 を選択して販売を完了できます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]

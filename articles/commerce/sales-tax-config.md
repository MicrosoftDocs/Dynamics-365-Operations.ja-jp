---
title: オンライン注文用の消費税のコンフィギュレーション
description: このトピックでは、Dynamics 365 Commerce のさまざまなオンライン注文タイプに対する消費税グループの選択の概要を示します。
author: gvrmohanreddy
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5801bbfb5b5850cb4c9ae06140bff5adca9b368febdc06d69c538fc49f9ee40a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772964"
---
# <a name="configure-sales-tax-for-online-orders"></a>オンライン注文用の消費税のコンフィギュレーション

[!include [banner](includes/banner.md)]

このトピックでは、宛先に基づく、または顧客アカウントに基づく税設定を使用して、異なるオンライン注文タイプに対する消費税グループの選択の概要を示します。 

電子商取引チャンネルで、注文の配送や集配などのオプションをサポートする必要があります。 消費税の適用は、オンライン顧客によって選択されたオプションに基づいて行われます。 

## <a name="destination-based-taxes-for-online-orders"></a>オンライン注文の宛先に基づく税

一般に、顧客の住所に送付されるオンライン注文の税は、宛先によって定義されます。 各消費税グループには、ビジネスが国または地域、都道府県、郡、市区町村などの出荷先の詳細を階層形式で定義できる、小売の宛先に基づく税コンフィギュレーションがあります。

### <a name="orders-delivered-to-customer-address"></a>顧客住所へ配送される注文

オンライン注文が行われると、Commerce 税エンジンにより、その注文の各明細行品目の配送先住所が使用され、宛先に基づく税基準が一致する消費税グループが検索されます。 たとえば、明細行品目の配送先がカリフォルニア州サンフランシスコになっているオンライン注文では、税エンジンにより、カリフォルニア州の消費税グループと消費税コードが検出され、それに応じて明細行品目ごとに税金が計算されます。

### <a name="order-pick-up-in-store"></a>店舗で受け取る注文

店舗での受け取りまたはカーブサイド ピックアップが指定されている注文明細行の場合は、選択したピックアップ店舗の税グループが適用されます。 特定の店舗の消費税を設定する方法の詳細については、[店舗のその他の税オプションの設定](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)を参照してください。

## <a name="customer-account-based-taxes-for-online-orders"></a>オンライン注文の顧客アカウントに基づく税

Commerce 本社の特定の顧客アカウントに消費税グループを構成する業務シナリオが存在する場合があります。 本社には、顧客アカウントに対して消費税を構成できる場所が 2 つあります。 そこにアクセスするには、まず **Retail と Commerce \> 顧客 \> 全ての顧客** の順に移動してから、顧客を選択して、顧客の詳細ページにアクセスする必要があります。

顧客アカウントに対して消費税を構成できる場所の 2 つは次のとおりです:

- 顧客の詳細ページの **請求書と出荷** クイック タブにある **消費税グループ**。 
- **住所の管理** ページの **一般** クイック タブにある **消費税**。 顧客の詳細ページからアクセスするには、**住所** クイックタブで特定の住所を選択してから、**詳細** を選択します。

> [!TIP]
> オンライン顧客注文の場合、宛先に基づく税のみを適用し、顧客アカウントに基づく税を回避する場合は、顧客の詳細ページの **請求書と出荷** クイックタブの **消費税グループ** フィールドが空であることを確認してください。 オンライン チャネルを使用してサインアップする新規顧客が、既定の顧客または顧客グループ設定から消費税グループ設定を継承しないようにするには、オンライン チャネルの既定の顧客設定および顧客グループ設定 (**Retail と Commerce \> 顧客 \> 顧客グループ**) に対する **消費税グループ** フィールドも空であることを確認してください。

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>宛先に基づく税または顧客アカウントに基づく税の適用を決定する 

次の表は、オンライン注文に対して宛先に基づく税または顧客アカウントに基づく税を適用するかどうかを示します。 

| 顧客タイプ | 出荷先住所                   | 顧客 > 請求書と出荷> 消費税グループ? | 本社の顧客アカウントの住所? | 顧客の住所 > 詳細 > 一般 > 消費税グループ?                                              | 適用される消費税グループ      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| ゲスト         | マンハッタン、NY                      | なし (空白)                                                | なし (空白)                              | なし (空白)                                                                                                   | NY (宛先に基づく税) |
| サインイン済み     | オースティン、TX                          | なし (空白)                                             | あり                               | None<br/><br/>オンライン チャネル経由で追加された新しいアドレス。                                                            | TX (宛先に基づく税) |
| サインイン済み     | サンフランシスコ、CA (店舗で受け取り) | あり (NY)                                            | 適用できません                              | 適用できません                                                                                                    | CA (宛先に基づく税) |
| サインイン済み     | ヒューストン、TX                         | あり (NY)                                            | あり                               | あり (NY)<br/><br/>オンライン チャネル経由で追加された新しい住所と、顧客アカウントから継承された消費税グループ。 | NY (顧客アカウントに基づく税)  |
| サインイン済み     | オースティン、TX                          | あり (NY)                                            | あり                               | あり (NY)<br/><br/>オンライン チャネル経由で追加された新しい住所と、顧客アカウントから継承された消費税グループ。 | NY (顧客アカウントに基づく税)  |
| サインイン済み     | サラソータ、FL                       | あり (NY)                                            | あり                               | あり (WA)<br/><br/>手動で WA に設定します。                                                                          | WA (顧客アカウントに基づく税)  |
| サインイン済み     | サラソータ、FL                       | なし (空白)                                                | あり                               | あり (WA)<br/><br/>手動で WA に設定します。                                                                          | WA (顧客アカウントに基づく税)  |

## <a name="additional-resources"></a>追加リソース

[宛先に基づくオンライン ストアの税を設定する](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[消費税の概要](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[[発生元] フィールドでの消費税計算方法](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[消費税の割り当ておよび上書き](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[消費税コードの合計額と間隔計算オプション](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[非課税の計算](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
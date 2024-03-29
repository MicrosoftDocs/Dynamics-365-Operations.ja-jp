---
title: 税コードの設定
description: この記事では、税計算サービスで税コードを設定する方法について説明します。
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 1bc250716763ce9d8e25c8850c8a3676bf65fb0c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862931"
---
# <a name="set-up-tax-codes"></a>税コードの設定

[!include [banner](../includes/banner.md)]

この記事では、税計算サービスで税コードを設定する方法について説明します。 これには、税コードを機能させる簡単なシナリオの設定と、複雑なシナリオに対するいくつかの詳細な税コード機能に関する情報が含まれます。

> [!IMPORTANT]
> 税計算サービスの税コードの設定は、法人に依存しません。 この設定は、Regulatory Configuration Service (RCS) で一度だけ実行できます。 Finance で選択した法人に対して税計算サービスを有効にした場合、税コードは Microsoft Dynamics 365 Finance に自動的に同期されます。

## <a name="simple-setup"></a>簡単な設定

税率が 1 つのみのシナリオなど、簡単なシナリオで税コードを使用するには、次の手順に従います。

1. [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) にサインインします。
2. **ワークスペース** \> **グローバリゼーション機能** \> **税計算** の順に移動します。
3. 設定する機能とバージョンを選択し、**編集** を選択します。
4. **全般** タブで、**構成バージョン** を選択します。
5. **税コード** タブで、**追加** を選択し、税コードと説明を入力します。
6. **計算基準** を選択します。 計算基準は、選択した税コンフィギュレーション バージョンで定義された一連の方法です。 この簡単なシナリオでは、**正味金額別** を選択します。
7. **保存** を選択します。 選択した計算基準に基づいて、使用可能なフィールドが増加します。
8. **レート** クイックタブで、**追加** を選択して、この税コードの税率を 1 つ追加します。
9. **保存** を選択します。

## <a name="calculation-origin"></a>計算元

計算基準は、税基準額と税額の計算方法を定義します。 これは、**電子申告** ワークスペースの税コンフィギュレーションによって構成されます。 **計算基準** フィールドでは、次の値を使用できます:

- 正味金額別
- 総額別
- 数量別
- 利益幅別
- 税の税

### <a name="by-net-amount"></a>正味金額別

**計算基準** フィールドで **正味金額別** を選択した場合、税額は、その他の税コードを除き、購入金額または売上金額の割合として計算されます。

たとえば、税率が 25% で、請求明細行には各 1.00 で品目数 10 が表示され、顧客に 10% の行割引が適用されるとします。 この場合、金額は次の方法で計算されます:

- **正味金額:** (10 × 1.00) – 10% = 9.00 
- **売上税:** 9.00 × 25% = 2.25 
- **合計請求金額:** 9.00 + 2.25 = 11.25

### <a name="by-gross-amount"></a>総額別

**計算基準** フィールドで **総額別** を選択すると、税額は総売上金額の割合として計算されます。 総額は、明細行の正味金額に、**計算基準** フィールドが **総額別** に設定されている税金を除く、明細行のすべての税および手数料を加えたものです。

たとえば、税務当局がある品目に特別関税を課したとします。 税額は、税金が計算される前の正味金額に加算されます。 次の税コードが使用されます:

- **関税 1** : 税率は 10% で、**正味金額別** の計算方法が使用されます。
- **関税 2** : 税率は 20% で、**正味金額別** の計算方法が使用されます。
- **税率** : 税率は 25% で、**総額別** の計算方法が使用されます。

正味金額が 10.00 の場合、関税 1 の金額は 1.00 (10.00 × 10%) で、関税 2 の金額は 2.00 (10.00 × 20%) です。 この場合、金額は次の方法で計算されます: 

- **総額:** 正味金額 + 関税 1 の金額 + 関税 2 の金額 = 10.00 + 1.00 + 2.00 = 13.00 
- **税額:** 13.00 × 25% = 3.25 
- **合計税額:** 1.00 + 2.00 + 3.25 = 6.25 
- **合計請求金額:** 10.00 + 6.25 = 16.25

### <a name="by-quantity"></a>数量別

**計算基準** フィールドで **数量別** を選択すると、税額は単位あたりの固定金額として計算され、ドキュメント明細行に入力された数量で乗算されます。 単位あたりの金額は、**レート** クイックタブで指定します。

たとえば、税コードが単位あたり 1.20 に設定されているとします。 売上請求書明細行では、25 単位の品目が販売されます。 この場合、税額は 25 × 1.20 = 30.00 と計算さます。

### <a name="by-margin"></a>利益幅別

**計算基準** フィールドで **利益幅別** を選択すると、税額は販売の利益幅の割合として計算されます。 販売の利益幅は、売上金額から原価金額を差し引いたものです。 この計算方法は、販売トランザクションにのみ適用されます。

たとえば、税率が 25% で、請求明細行には各 10.00 で品目数 10 が表示され、品目あたりの原価が 6 であるとします。 この場合、金額は次の方法で計算されます:

- **販売利益幅:** 10 × ( 10.00 – 6.00) = 40.00
- **税額:** 40.00 × 25% = 10.00
- **合計請求金額:** 100.00 + 10.00 = 110.00

### <a name="tax-on-tax"></a>税の税

**計算基準** フィールドで **税の税** を選択した場合、売上税は、同じドキュメント明細行の他のすべての税額に対する割合として計算されます。

たとえば、次の税コードが使用されます:

- **関税 1** : 税率は 10% で、**正味金額別** の計算方法が使用されます。
- **関税 2** : 税率は 20% で、**正味金額別** の計算方法が使用されます。
- **関税に対する税金** – 税率は 25% で、**税の税** の計算方法が使用されます。

この場合、金額は次の方法で計算されます:

- **正味金額:** 10.00 
- **関税 1:** 10.00 × 10% = 1.00 
- **関税 2:** 10.00 × 20% = 2.00 
- **関税に対する税金:** 3.00 × 25% = 0.75
- **税合計:** 1.00 + 2.00 + 0.75 = 3.75 
- **合計請求金額:** 10.00 + 3.75 = 13.75

## <a name="advanced-functionality"></a>詳細機能

このセクションでは、複雑なシナリオに対する税コード設定の詳細な機能について説明します。

### <a name="tax-exemption"></a>課税控除

**全般** クイック タブで **免税対象である** オプションを **はい** に設定すると、実際の税率に関係なく、税額は常に 0 (ゼロ) に上書きされます。

**控除コード** フィールドを設定して、控除の理由を指定することができます。 

**控除コード** フィールドに対してマスター データ検索を有効にできます。 この方法により、Finance で定義されている控除コード値の中から選択できます。 マスター データ検索を有効にする方法の詳細については、[税計算コンフィギュレーションのマスター データ検索の有効化](tax-service-set-up-environment-master-data-lookup.md) を参照してください。

たとえば、税率が 25% で、税コードで **免税対象である** オプションが **はい** に設定されているとします。 請求明細行には、各 1.00 で品目数 10 が表示され、顧客には 10% の行割引が適用されます。 この場合、金額は次の方法で計算されます:

- **正味金額:** (10 × 1.00) – 10% = 9.00 
- **売上税:** 0.00 
- **合計請求金額:** 9.00 + 0.00 = 9.00

### <a name="use-tax"></a>使用税

**全般** クイックタブで **使用税である** オプションを **はい** に設定すると、税額が **仕入先の集計** 勘定ではなく **使用税支払** 勘定に転記されます。

たとえば、税率が 25% で、税コードで **使用税である** オプションが **はい** に設定されているとします。 請求明細行には、各 1.00 で品目数 10 が表示され、顧客には 10% の行割引が適用されます。 この場合、金額は次の方法で計算されます:

- **正味金額:** (10 × 1.00) – 10% = 9.00 
- **使用税:** 9.00 × 25% = 2.25
- **合計請求金額:** 9.00 + 0.00 = 9.00

> [!IMPORTANT]
> **免税対象である** オプションと **使用税である** オプションの両方が税コードで **はい** に設定されている場合、このコードは販売トランザクションでは免税、購買トランザクションでは使用税として認識されます。

### <a name="reverse-charges"></a>逆請求

**全般** クイックタブで **逆請求である** オプションを **はい** に設定した場合、税率をマイナスとして構成できます。 逆請求のシナリオでは、2 つの税コードを設定することをお薦めします: 1 つは正の税率で、もう 1 つは負の税率です。 両方の税コードが同じ税率値であり、負の税率を持つ税コードで **逆請求である** オプションが **はい** に設定されている必要があります。 Finance の逆請求ソリューションの詳細については 、[VAT/GST スキームの逆請求メカニズム](emea-reverse-charge.md)を参照してください。

たとえば、1 つの請求明細行に対して 2 つの税コードが決定されます。 一方の税率は 25% です。 もう一方の税率は -25% で、2 つ目の税コードの **逆請求である** オプションが **はい** に設定されています。 請求明細行には、各 1.00 で品目数 10 が表示されています。 この場合、金額は次の方法で計算されます:

- **正味金額:** (10 × 1.00) = 10.00 
- **税コード 1:** 10.00 × 25% = 2.50
- **税コード 2:** 10 × -25% = -2.50
- **合計請求金額:** 10.00 + 2.50 -2.50 = 10.00

### <a name="exclusion-from-base-amount-calculations"></a>基準額計算からの除外

**全般** クイックタブで **基準額計算から除外** オプションを **はい** に設定すると、税金コードの計算された税額が、価格を含むシナリオで他の税コード計算の税基準額から除外されます。

詳細については、[価格に税金が含まれる場合の価格上の税金の計算が有効](global-exclude-from-tax-base-amount-calculation.md) を参照してください。

### <a name="rates"></a>レート

**レート** クイックタブでは、税基準額のさまざまな範囲に対して異なる税率を定義できます。 税額を計算するために、税額計算サービスは常に税基準額に一致するレートを使用します。

たとえば、税率は次の表に示すように構成できます。

| 最小額 | 最大時間数 | 税率   |
| -------------- | -------------- | ---------- |
| 0              | 1.000          | 10% |
| 1.000          | 5,000          | 15% |
| 5,000          | 10,000         | 20% |
| 10,000         | 0              | 30% |

この場合、税額は次の方法で計算されます:

- 税基準額が 300.00 の場合、税率は 10% で、税額は 300.00 × 10% = 30.00 です。
- 税基準額が 3,000.00 の場合、税率は 15% で、税額は 3,000.00 × 15% = 450.00 です。
- 税基準額が 6,000.00 の場合、税率は 20% で、税額は 6,000.00 × 10% = 1,200.00 です。
- 税基準額が 20,000.00 の場合、税率は 30% で、税額は 20,000.00 × 30% = 6,000.00 です。

> [!NOTE]
> 税基準額が一方の明細行の最大金額と他方の明細行の最小金額の両方に一致する場合、基準額は最小基準額に一致する税率を使用します。 たとえば、税基準額が 1000.00 の場合、税率は 15% で、税額は 1,000.00 × 15% = 150.00 です。

### <a name="limits"></a>制限

**制限** クイックタブでは、税額が最小/最大範囲内にある場合に、計算された税額を上書きするように税の上限を定義できます。

- 計算された税額が、**制限** クイックタブで構成される最大税額以上の場合、最終的な税額は最大税額と等しくなります。
- 計算された税額が **制限** クイックタブで構成された最小税額よりも小さい場合、最終的な税額は 0 (ゼロ) になります。

たとえば、税の上限は次のように構成されます:

- **最小税額:** 100 
- **最大税額:** 1,000

計算された税額が 2,000 の場合、最終的な税額は 1,000 となります。

計算された税額が 500 の場合、最終的な税額は 500 となります。

計算された税額が 80 の場合、最終的な税額は 0 (ゼロ) となります。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

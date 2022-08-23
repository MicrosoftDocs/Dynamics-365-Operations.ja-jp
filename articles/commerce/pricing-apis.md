---
title: Commerce 価格 API
description: この記事では、Microsoft Dynamics 365 Commerce の価格エンジンが提供する様々な価格 API について説明します。
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294119"
---
# <a name="commerce-pricing-apis"></a>Commerce 価格 API

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の価格エンジンが提供する様々な価格 API について説明します。

Dynamics 365 Commerce 価格エンジンは、様々な価格設定シナリオをサポートするために、外部アプリケーションから消費可能な以下の Retail Server API を提供します:

- **GetActivePrices** - この API は、簡単な割引を含む製品の算出価格を取得します。
- **CalculateSalesDocument** - この API は、一緒に購入した場合に、指定された数量の製品の価格と割引を計算します。
- **GetAvailablePromotions** - この API は、買い物カゴの製品に適用される割引を受け取ります。 
- **AddCoupons** - この API は、カートにクーポンを追加します。
- **RemoveCoupons** - この API は、カートからクーポンを削除します。

Retail Server API を外部アプリケーションで利用する方法の詳細については、[外部アプリケーションで Retail Server API を利用する](dev-itpro/consume-retail-server-api.md) を参照してください。

## <a name="getactiveprices"></a>GetActivePrices

*GetActivePrices* API は、Commerce バージョン 10.0.4 のリリースで導入されました。 この API は、簡単な割引を含む製品の算出価格を取得します。 複数行の割引は計算されず、API リクエストの各商品は数量が 1 であると仮定されます。 また、この API は、製品の一覧を入力として受け取り、個々の製品の価格を一括してクエリできます。

*GetActivePrices* API は、**従業員**、**顧客**、**匿名**、**アプリケーション** コマースのロールをサポートします。

*GetActivePrices* API の主なユースケースは、商品詳細ページ (PDP) で、小売業者は有効な割引を含む商品のベスト プライスを紹介したいと考えます。

次の表に、*GetActivePrices* API の入力パラメータを示します。

| Name                                    | サブ名称 | 種類 | 必須/任意 | Description |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | 必須 | |
|                                         | ChannelId | long | 必須 | |
|                                         | CatalogId | long | 必須 | |
| productIds                              | | IEnumerable\<long\> | 必須 | 価格計算を行う製品のリストです。 |
| activeDate                              | | DateTimeOffset | 必須 | 価格が計算される日付。 |
| customerId                              | | 文字列 | オプション | 顧客 取引先企業番号。 |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | オプション | アフィリエイト層とロイヤリティ層。 |
|                                         | AffiliationId | long | 必須 | 系列 ID。 |
|                                         | LoyaltyTierId | long | オプション | ロイヤルティ層 ID。 |
| includeSimpleDiscountsInContextualPrice | | ブール | オプション | 価格決定の算定に単純な割引を含める場合は、このパラメーターを **true** に設定します。 既定値は **false** です。 |
| includeVariantPriceRange                | | ブール | オプション | マスタ 製品のすべてのバリアント間で最小価格および最大価格を取得するには、このパラメータを **true** に設定します。 既定値は **false** です。 |
| includeAttainablePricesAndDiscounts     | | ブール | オプション | 達成可能な価格と割引を取得するには、このパラメータを **true** に設定します。 既定値は **false** です。 |

**サンプル要求本文**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**応答本文の例**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

*CalculateSalesDocument* API は、Commerce バージョン 10.0.25 のリリースで導入されました。 この API は、一緒に購入した場合に、指定された数量の製品の価格と割引を順番に計算します。 *CalculateSalesDocument* API の後の価格決定の算定では、単一行割引と複数行割引の両方が考慮されます。

*CalculateSalesDocument* API の主な使用例は、完全なカート コンテキストが維持されないシナリオ (販売見積など) での価格決定の算定です。 この場合、POS や Commerce e コマースのシナリオにも役立ちます。 カート内の品目がセットで計算される場合 (ばらばらのバンドル、リンク商品、おすすめ商品、既にカートに入れてある商品など)、合計金額が安くなれば、顧客は製品をカートに追加できる可能性があります。

*CalculateSalesDocument* API のリクエスト、レスポンスともにデータ モデルは **Cart** です。 ただし、この API のコンテキストでは、データ モデルは **SalesDocument** となっています。 プロパティのほとんどはオプションであり、価格算定に影響を与えるものはごくわずかであるため、以下の表では価格に関連するフィールドのみが表示されます。 他のフィールドを API リクエストに関連させることは推奨しません。

*CalculateSalesDocument* API のスコープは、価格と割引の算定のみです。 税金や費用は含まれません。

次の表に、**salesDocument** という名前のオブジェクト内の入力パラメーターを示します。

| Name             | サブ名称 | 種類 | 必須/任意 | Description |
|------------------|----------|------|-------------------|-------------|
| ID               | | 文字列 | 必須 | 営業ドキュメントの識別子。 |
| CartLines        | | IList\<CartLine\> | オプション | 価格や割引を計算するラインの一覧です。 |
|                  | 製品 ID | long | CartLine のスコープで必須 | 製品レコード ID。 |
|                  | ItemId | 文字列 | オプション | 品目識別子。 値を指定する場合は、**ProductId** パラメータの値と一致させる必要があります。 |
|                  | InventoryDimensionId | 文字列 | オプション | 在庫分析コードの識別子です。 値が提供される場合、**ItemId** と **InventoryDimensionId** の値の組み合わせは **ProductId** パラメータの値と一致る必要があります。 |
|                  | Quantity | decimal | CartLine のスコープで必須 | 製品の数量。 |
|                  | UnitOfMeasureSymbol | 文字列 | オプション | 製品の単位。 既定では、値が提供されない場合、API は商品の販売単位を使用します。 |
| CustomerId       | | 文字列 | オプション | 顧客 取引先企業番号。 |
| LoyaltyCardId    | | 文字列 | オプション | このロイヤルティ カードの識別子です。 ロイヤルティ カードに関連する顧客アカウントは、**CustomerId** パラメータの値 (指定されている場合) と一致する必要があります。 ロイヤルティ カードは、ロイヤルティ カードが見つからないか、ステータスが **ブロック** の場合は考慮 されません。 |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | オプション | アフィリエイト ロイヤリティの階層ライン。 **CustomerId** 値および/または **LoyaltyCardId** 値が指定された場合、対応する所属ロイヤリティ層の行は、**AffiliationLines** 値で指定された行にマージされます。 |
|                  | AffiliationId | long | AffiliationLoyaltyTier のスコープで必須 | アフィリエイト レコード ID。 |
|                  | LoyaltyTierId | long | AffiliationLoyaltyTier のスコープで必須 | ロイヤルティ層レコード ID。 |
|                  | AffiliationTypeValue | int | AffiliationLoyaltyTier のスコープで必須 | アフィリエイト行が **全般** タイプ (**0**) か **ロイヤルティ** タイプ (**1**) かを示す値。 このパラメータが **0** に設定されている場合、API は **AffiliationId** の値を識別子として受け取り、**LoyaltyTierId** 値を無視します。 このパラメータが **1** に設定されている場合、API は **LoyaltyTierId** の値を識別子として受け取り、**AffiliationId** 値を無視します。 |
|                  | ReasonCodeLines | 取立\<ReasonCodeLine\> | AffiliationLoyaltyTier のスコープで必須 | 理由コードの行。 このパラメータは価格算定には影響しませんが、**AffiliationLoyaltyTier** オブジェクトの一部として必要です。 |
|                  | CustomerId | 文字列 | AffiliationLoyaltyTier のスコープで必須 | 顧客 取引先企業番号。 |
| クーポン          | | IList\<Coupon\> | オプション | 適用されないクーポン (非アクティブ、期限切れ、見つからない場合) は、価格算定の対象にはなりません。 |
|                  | コード | 文字列 | クーポンのスコープで必須 | クーポン コード。 |
|                  | CodeId | 文字列 | オプション | クーポン コードの識別子。 値を指定する場合は、**Code** パラメータの値と一致させる必要があります。 |
|                  | DiscountOfferId | 文字列 | オプション | 割引識別子。 値を指定する場合は、**Code** パラメータの値と一致させる必要があります。 |

**サンプル要求本文**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

カートのオブジェクト全体が応答本文として返されます。 価格や割引を確認するには、次のテーブルのフィールドに注目する必要があります。

| Name           | サブ名称 | 種類 | Description |
|----------------|----------|------|--------------|
| NetPrice       | | decimal | 割引適用前の売上ドキュメント全体の正味価格。 |
| DiscountAmount | | decimal | 売上ドキュメント全体の割引額の合計。 |
| TotalAmount    | | decimal | 売上ドキュメント全体の合計金額。 |
| CartLines      | | IList\<CartLine\> | 価格と割引の詳細を含む計算済の明細行。 |
|                | 価格 | decimal | 製品の単価。 |
|                | NetPrice | decimal | 割引適用前の明細の正味価格 (= *価格* &times; *数量*)。 |
|                | DiscountAmount | decimal | 割引金額。 |
|                | TotalAmount | decimal | 明細行の最終的な価格合計の結果。 |
|                | PriceLines | IList\<PriceLine\> | 価格のソース (基準価格、価格調整、取引契約など)、金額などの価格の詳細。 |
|                | DiscountLines | IList\<DiscountLine\> | 割引の詳細。 |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

複数のカート明細行を持つカートがある場合、*GetAvailablePromotions* API はカート明細行に適用されるすべての割引を返します。 

*GetAvailablePromotions* API の主な使用例はカートページです。小売業者は現在のカートで適用された割引や利用可能なクーポンを表示することができます。

次の表に、*GetAvailablePromotions* API の入力パラメータを示します。

| Name        | 種類 | 必須/任意 | Description |
|-------------|------|-------------------|-------------|
| キー         | 文字列 | 必須 | カート ID。 |
| cartLineIds | IEnumerable\<string\> | オプション | このパラメータは、選択されたカート行の割引のみを返すように設定します。 |

**応答本文の例**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

*AddCoupons* API では、カートにクーポンの一覧を追加できます。 クーポンを追加した後、カートのオブジェクトを返します。

次の表に、*AddCoupons* API の入力パラメータを示します。

| Name                 | 種類 | 必須/任意 | Description |
|----------------------|------|-------------------|-------------|
| キー                  | 文字列 | 必須 | カート ID。 |
| couponCodes          | IEnumerable\<string\> | 必須 | カートに追加するクーポンコード。 |
| isLegacyDiscountCode | ブール | オプション | このパラメータを **true** に設定すると、クーポンがレガシー割引コードであることを示します。 既定値は **false** です。 |

## <a name="removecoupons"></a>RemoveCoupons

The *RemoveCoupons* API は、カートからクーポンのリストを削除することができます。 クーポンを削除した後、カートのオブジェクトを返します。

次の表に、*RemoveCoupons* API の入力パラメータを示します。

| Name        | 種類 | 必須/任意 | Description |
|-------------|------|-------------------|-------------|
| キー         | 文字列 | 必須 | カート ID。 |
| couponCodes | IEnumerable\<string\> | 必須 | カートから削除するクーポンコードです。 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

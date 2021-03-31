---
title: 請求書照合と会社間発注
description: 会社間の売買取引に関連する購買側の法人が、買掛金勘定の請求書照合を使用する設定になる場合があります。 その場合、会社間の売買取引と買掛金勘定の請求書照合の両方の転記要件が合っていないと、会社間仕入先請求書は転記できません。
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: roschlom
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4af4251580b66895d4dd284a2984d47fddc77066
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221036"
---
# <a name="invoice-matching-and-intercompany-purchase-orders"></a>請求書照合と会社間発注

[!include [banner](../includes/banner.md)]

会社間の売買取引に関連する購買側の法人が、買掛金勘定の請求書照合を使用する設定になる場合があります。 **買掛金管理パラメーター** フォームの **不一致のある請求書を転記** フィールドが **承認の要求** に設定されている場合は、請求書照合検証が実行されます。 その場合、会社間の売買取引と買掛金勘定の請求書照合の両方の転記要件が合っていないと、会社間仕入先請求書は転記できません。

このトピックの例では、会社間取引に次の設定を使用します:
-   Fabrikam Purchase は、購買側の法人です。
-   Fabrikam Sales は、販売側の法人です。
-   顧客 4020 が Fabrikam Sales に存在します。
-   仕入先 3024 が Fabrikam Purchase に存在します。
-   Fabrikam Purchase では、会社間の情報がベンダー 3024 に指定されています。 Fabrikam Sales は顧客会社として指定され、顧客 4020 は Fabrikam Purchase 法人に対応する顧客アカウントとして指定されています。
-   Fabrikam Sales では、顧客 4020 の会社間の情報が指定されています。 Fabrikam Purchase はベンダー会社として指定され、ベンダー 3024 は Fabrikam Sales 法人に対応するベンダー アカウントとして指定されています。

これらの例では、Fabrikam Purchase の買掛金勘定の請求書照合に以下の設定を使用します。
-   買掛金勘定パラメーター ページで [請求書照合の検証を有効化] オプションが選択されます。
-   買掛金管理パラメーター ページの [不一致のある請求書を転記] フィールドが [承認の要求] に設定されます。
-   この法人の価格許容値の割合は 2% です。

## <a name="example-price-matching-and-intercompany-trade"></a>例 : 価格照合と会社間売買
会社間仕入先請求書と会社間顧客請求書の正味金額は同額でなければなりません。 この要件は、該当するいかなる請求書照合の承認または価格許容率よりも優先します。 たとえば、次のように設定します。
1.  Fabrikam Purchase で、顧客 4020 の販売注文 SO888 を作成します。 Fabrikam Purchase に、仕入先 3024 に会社間発注書 ICPO222 が自動的に作成され、Fabrikam Sales では、販売注文 ICSO888 が自動的に作成されます。
2.  Fabrikam Sales に、品目が受領済みであると登録し、梱包明細を転記します。 ICSO888 の状態が [出荷済み] に変更されます。 ICPO222 の状態が [受入済] に変更されます。
3.  Fabrikam Sales で、ICSO888 の請求書を更新します。 単価 0.45 で数量 100 が更新されます。
4.  Fabrikam Purchase で、ICPO222 の請求書を作成します。 誤って正味価格を 45.00 から 54.00 に変更しました。 価格が 2% の価格許容率を超えていることを示すアイコンが表示されます。
5.  請求書照合の詳細ページで、[照合不一致を伴う転記を承認する] オプションを選択します。 仕入先請求書ページで、[OK] をクリックします。 仕入先請求書が会社間仕入先請求書ではない場合、転記できます。 しかし、処理しているのは会社間仕入先請求書なので、転記できません。 会社間の売買取引で、会社間販売注文書の請求合計金額は、対応する会社間発注の請求合計金額と一致していなければなりません。 この問題を解決するため、正味価格を既定の金額 45.00 に戻して、請求書の正味価格を修正する必要があります。

## <a name="example-quantity-matching-with-intercompany-trade"></a>例 : 会社間取引の数量照合
会社間発注書と会社間販売注文書の数量は一致していなければなりません。 この要件は、該当する請求書照合のいかなる承認よりも優先します。 この例では、会社間取引で以下の追加設定を使用します。
-   Fabrikam Purchase で、仕入先 3024 の発注書のアクション ポリシーを、元の顧客請求書と会社間仕入先請求書の両方で自動的に転記するよう設定します。

この例では、Fabrikam Purchase に、以下の追加の買掛金勘定の請求書照合の設定を使用します。
-   品目 B-R14 で使用するモデル グループの品目モデル グループのページで、入荷の条件のオプションを選択します。
-   品目 B-R14 の手持数量は 0 です。

たとえば、次のように設定します。
1.  Fabrikam Purchase で、顧客 4020 の販売注文 SO999 を作成します。 この注文には 1 つの明細行品目 : 電池 100 個 (品目 B-R14)、単価 1.00 があります。 Fabrikam Purchase に、仕入先 3024 に会社間発注書 ICPO333 が自動的に作成され、Fabrikam Sales では、販売注文 ICSO999 が自動的に作成されます。
2.  Fabrikam Sales で ICSO999 の請求書を更新します。 品目が在庫切れで、まだ受領されていないので、転記は失敗します。 したがって、財務情報は更新できません。
3.  Fabrikam Sales で、品目の受領を登録し、ICSO999 の梱包明細を転記します。 ICPO333 の製品受領書が Fabrikam Purchase に自動的に転記されます。 Fabrikam Purchase の品目 B-R14 の受領数量は 100 に変化します。
4.  Fabrikam Sales で ICSO999 の請求書を更新します。 両方の法人で転記が成功します。 Fabrikam Purchase の品目 B-R14 の購買済数量は 100 に変化します。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
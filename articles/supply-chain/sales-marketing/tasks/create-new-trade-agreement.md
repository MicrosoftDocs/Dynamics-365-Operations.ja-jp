---
title: 新しい売買契約の作成
description: この手順は、特定の顧客と合意した新しい製品販売価格を登録する売買契約の作成方法を示します。
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24290ec873da9e871c001bcdc97e14dcad0e3d1e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111110"
---
# <a name="create-a-new-trade-agreement"></a>新しい売買契約の作成

[!include [banner](../../includes/banner.md)]

この手順は、特定の顧客と合意した新しい製品販売価格を登録する売買契約の作成方法を示します。 この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。 独自のデータを使用する場合は、このガイドの開始する前に、"価格 (販売)" に既定の取引関係が設定されている売買契約仕訳帳名が存在することを確認する必要があります。

## <a name="create-and-post-a-new-trade-agreement-journal"></a>新しい売買契約仕訳帳の作成と転記

1. **ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 価格と割引 > 売買契約仕訳帳** の順に移動します。
2. **新規** をクリックします。
3. **名前** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、目的のレコードを見つけ、選択します。
5. **アクション ウィンドウ** で、**明細行** をクリックします。
6. **アカウント コード** フィールドで、「テーブル」を選択します。
    
    この例では、特定の顧客の価格を更新しており、これはテーブルの選択が必要であることを意味しています。 製品の表示価格を更新する場合は、新しい価格がすべての顧客に対して有効になるように、「すべて」を選択します。 異なる顧客の区分間の価格を区別する場合は、[グループ] を選択します。 [グループ] を選択するには、[顧客の価格グループ] を設定しておく必要があります。  

7. **勘定の選択** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
8. 一覧で、目的のレコードを見つけ、選択します。
9. **品目コード** フィールドで、「テーブル」を選択します。
    
    「価格 (販売)」タイプの売買契約を入力する場合は、**品目コード** フィールドで「テーブル」のみを選択する必要があります。 これは、価格が絶対値であり、すべての製品または製品のグループで同じにすることができないためです。
    
10. **品目関係** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
11. リストで、契約に含める製品を選択します。 選択した製品をメモします。  
12. **ソース** フィールドに、最小数量を入力します。
    - 新しい価格を利用する前に、顧客が最小数量を注文する必要がある場合、ここでその数量を指定する必要があります。  
    - 契約の価格が有効にならない最大数量を指定するには、**ターゲット** フィールドに値を入力します。 複数の数量区分に基づいて価格と割引を提供する場合、**ソース** と **ターゲット** フィールドそれぞれに最小数量と最大数量のペアとして各数量の区分を指定します。
13. **通貨金額フィールド** に価格を入力します。
14. **詳細** セクションの **開始日** フィールドに、この契約が有効になる日付を入力します。
15. **保存** をクリックします。
16. **検証** をクリックします。
17. **選択した明細行の検証** をクリックします。
18. **OK** をクリックします。
19. **転記** をクリックします。
20. **OK** をクリックします。

## <a name="view-trade-agreements-for-a-product"></a>製品に関連する売買契約の表示

1. **ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > リリース済製品** の順に移動します。
2. リストで、更新した価格の製品を見つけ、選択します。
3. **アクション ウィンドウ** で、**販売** をクリックします。
4. **売買契約の表示** をクリックします。
    
    作成した価格の売買契約の詳細を確認します。

5. ページを閉じます。

## <a name="additional-resources"></a>追加リソース

### <a name="whitepaper"></a>ホワイト ペーパー

詳細については、次のホワイト ペーパー (AX2012 をサポートするように記述されているが、Dynamics 365 Supply Chain Management にも適用される) をダウンロードしてください

- [売買契約](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a>コミュニティのブログ

- [財務と運用での販売価格](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

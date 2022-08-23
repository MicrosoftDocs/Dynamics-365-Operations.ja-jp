---
title: コール センター注文の作成
description: この記事では、コール センター ユーザーが Microsoft Dynamics 365 Commerce で顧客の検索、新しい注文の作成、製品の検索、および顧客からの支払の回収を行う手順の例についてに説明します。
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228513"
---
# <a name="create-call-center-orders"></a>コール センター注文の作成

[!include [banner](../includes/banner.md)]

この記事では、コール センター ユーザーが Microsoft Dynamics 365 Commerce で顧客の検索、新しい注文の作成、製品の検索、および顧客からの支払の回収を行う手順の例についてに説明します。 手順では、USRT デモ データの会社を使用して、販売注文の担当者を対象としています。 

## <a name="prerequisites"></a>必要条件

手順を完了するユーザーは、コール センターのユーザーとして設定されている必要があります。 必要に応じて、Fabrikam の半年毎のカタログを少なくとも 1 つのソース コードと共に公開できます。

### <a name="add-yourself-as-a-call-center-user"></a>ユーザー自身をコール センター ユーザーとして追加する

ユーザー自身をコール センター ユーザーとして追加するには、次の手順に従います。

1. Commerce headquarters で、**小売とコマース \> チャネル \> コール センター \> すべてのコール センター** に移動します。
1. **ユーザー** フィールドで **チャネル ユーザー** を選択します。
1. アクション ウィンドウで、**新規** を選択します。
1. **ユーザー ID** フィールドに、ユーザー ID を入力します。
1. **名前** フィールドで、ユーザー名を入力します。 ユーザー名は、ユーザー ID と同じにすることができます。
1. アクション ウィンドウで、**保存** を選択します。
1. **小売とコマース \> チャネル \> コール センター \> すべてのコール センター** に戻ります。
1. コール センターの小売チャネル ID を選択します。
1. **オーダー完了の有効化** オプションが **はい** に設定されていることを確認します。 オプションが表示されない場合は、この手順を省略できます。

## <a name="complete-the-example-call-center-procedure"></a>コール センターの手順例を完了する

コール センターの手順例を完了するには、次の手順に従います。

1. **Retail と Commerce \> 顧客 \> 顧客サービス** に移動します。
1. **顧客検索** タブで、顧客を検索するための検索条件を入力します。 この例の手順では、**Karen** を入力します。
1. **検索** を選択します。 **顧客検索** ダイアログ ボックスが表示され、検索結果の一覧が表示されます。
1. 顧客 ID 番号 **2001** の **Karen Berg** の顧客レコードを選択し、**選択** を選択します。
1. アクション ウィンドウで **新しい販売注文** を選択します。
1. 右側で **ヘッダー** タブを選択します。
1. **配送** FastTab の **配送方法** フィールドで、**99 標準** を選択します。

    ![配送モードの選択。](../media/Select_Mode_of_Delivery.png)

1. 右側で **明細行** タブを選択します。
1. **販売注文明細行** セクションで、新しい販売明細行の新しい行にある **品目番号** フィールドに、検索する品目番号を入力します。 この例の手順では **81327** と入力し、ドロップダウン リストで製品を選択して販売注文に追加します。
1. **数量** フィールドに、販売数量を入力します。
1. **ソース コード** フィールドで、カタログのソース コードを選択します。 有効なソース・コードがない場合、この手順を省略できます。
1. アクション ウィンドウで、顧客支払を取得するために **完了** を選択します。 このアクションにより、**販売注文集計** ダイアログ ボックスが開き、支払期限のある合計金額が表示されます。 また、このアクションによって出荷および取扱いなどのすべての費用の算定もトリガーされ、**販売注文集計** ダイアログ ボックスに表示されます。

    ![完了ボタン。](../media/Complete_button.png)

1. **販売注文集計** ダイアログ ボックスの **支払** FastTab で、**追加** を選択して支払をキャプチャします。

    ![販売注文集計ダイアログ ボックス。](../media/order_summary.png)

1. **顧客支払情報の入力** ダイアログ ボックスにある **支払方法** フィールドで、支払方法を選択します。 この例の手順では、**現金** を選択します。
1. **支払額** フィールドに支払額を入力します。 この例では、**120.00** と入力します。これは、**販売注文集計** ダイアログ ボックスに表示される注文残高に相当します。 この金額を入力すると、全額支払い済みとして注文を完了できます。
1.  **OK** を選択します。
1. **送信** を選択します。

## <a name="additional-resources"></a>追加リソース

[配送モードによるトランザクション メールのカスタマイズ](../customize-email-delivery-mode.md)

[POS での荷渡方法の変更](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

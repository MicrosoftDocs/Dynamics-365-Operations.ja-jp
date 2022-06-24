---
title: 税が伝票の誤った勘定科目に転記される
description: この記事では、税金が伝票の間違った勘定科目に転記される際に役立つトラブルシューティング情報を提供します。
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 5eb0f7d0196ac52a87d61cba6b9cd438708eff73
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846744"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>税金が伝票の間違った勘定科目に転記される

[!include [banner](../includes/banner.md)]

転記時に、税金が伝票の間違った勘定科目に転記される場合があります。 この問題のトラブルシューティングを行う場合は、必要に応じて次のセクションの手順に従います。 この記事の例では、販売注文をビジネス ドキュメントとして使用します。

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>間違って転記された税トランザクションの税コードの検索

1. **伝票トランザクション** ページで、使用するトランザクションを選択し、**転記済消費税** を選択します。

    [![伝票トランザクション ページの転記済消費税ボタン。](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. **消費税コード** フィールドの値を確認します。 この例の場合、**VAT 19** です。

    [![転記済消費税ページの消費税コード フィールド。](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>税コードの元帳転記グループの確認

1. **税** \> **間接税** \> **消費税** \> **消費税コード** の順に移動します。
2. 税コードを検索して選択し、**元帳転記グループ** フィールドの値を確認します。 この例の場合、**VAT** です。

    [![消費税コード ページの元帳転記グループ フィールド。](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. **元帳転記グループ** フィールドの値は、リンクです。 グループのコンフィギュレーションの詳細を表示するには、リンクを選択します。 または、フィールドを選択したまま (または右クリック) にして、**詳細の表示** を選択します。

    [![詳細を表示コマンド。](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. **消費税支払** フィールドで、トランザクション タイプに従って勘定番号が正しいか確認します。 正しくない場合は、転記する適切な勘定を選択します。 この例では、販売注文の消費税は消費税支払の勘定 222200 に転記されます。

    [![元帳転記グループ ページの消費税支払フィールド。](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    次の表に、**元帳転記グループ** ページの各フィールドに関する情報を示します。

    | フィールド                  | 説明 |
    |------------------------|-------------|
    | 消費税支払      | 税務当局に消費税を支払う主勘定。 |
    | 消費税収入   | 税務当局から税金を受け取る主勘定。 |
    | 使用税経費        | 仕入先が、欧州連合 (EU) の逆請求の商品及びサービス税 (GST) または統合売上税 (HST) の一部として税務当局に申告または報告しない、控除可能な使用税を転記するために使用する主勘定。 **使用税** は、トランザクションに使用する消費税グループの消費税コードに対して選択する必要があります。 このフィールドは、**総勘定元帳のパラメーター** ページの **売上税課税ルールの適用** が選択されている場合には使用できません。 |
    | 使用税支払勘定        | 税務当局に支払う使用税を転記するために使用する主勘定。 |
    | 決済勘定     | **使用税支払勘定** および **消費税収入** フィールドで指定された勘定科目の正味残高を転記するために使用する主勘定。 |
    | 仕入先現金割引   | この元帳転記グループと関連付けられた消費税コードについての現金割引を転記するために使用する主勘定。 |
    | 顧客現金割引 | この元帳転記グループと関連付けられた消費税コードについての現金割引を転記するために使用する主勘定。 |

    詳細については、[売上税の元帳転記グループの設定](tasks/set-up-ledger-posting-groups-sales-tax.md)を参照してください

## <a name="debug-in-code-to-check-ledger-dimensions"></a>コードをデバッグして勘定分析コードを確認する

このコードでは、転記勘定は勘定分析コードによって決まります。 勘定分析コードは、勘定のレコード ID をデータベースに保存します。

1. 販売注文の場合、**Tax::saveAndPost()** および **Tax::post()** メソッドにブレークポイントを追加します。 **\_ledgerDimension** の値に注意してください。

    [![ブレークポイントが設定された販売注文コード サンプル。](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    発注書の場合は、**TaxPost::saveAndPost()** および **TaxPost::postToTaxTrans()** メソッドにブレークポイントを追加します。 **\_ledgerDimension** の値に注意してください。

    [![ブレークポイントが設定された発注書コード サンプル。](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. 次の SQL クエリを実行して、勘定分析コードで保存されるレコード ID に基づいて、データベース内の勘定の表示値を検索します。

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![レコード ID の表示値。](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. コール スタックを確認して、**_ledgerDimension** の値が割り当てられている場所を検索します。 通常、この値は **TmpTaxWorkTrans** から取得されます。 この場合、**TmpTaxWorkTrans::insert()** および **TmpTaxWorkTrans::update()** にブレークポイントを追加して、値が割り当てられている場所を検索する必要があります。

## <a name="determine-whether-customization-exists"></a>カスタマイズが存在するかどうかの確認

前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。 カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

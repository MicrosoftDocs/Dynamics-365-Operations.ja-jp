---
title: TaxTrans レコードが生成されない
description: このトピックでは、TaxTrans レコードが生成されない場合に役立つトラブルシューティング情報を提供します。
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947667"
---
# <a name="taxtrans-record-isnt-generated"></a>TaxTrans レコードが生成されない

[!include [banner](../includes/banner.md)]

トランザクションの **転記済売上税** を選択したが、**転記済売上税** ページに税明細行が表示されていないか、税明細行がない場合は、**TaxTrans** レコードが生成されていない可能性があります。

[![明細行がない品目の転記済売上税ページ](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

この問題のトラブルシューティングを行う場合は、必要に応じて次のセクションの手順に従います。

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>トランザクションを転記する前に売上税を確認する

1. トランザクションを転記する前に、**請求の転記** ページで、**売上税** を選択して計算を確認します。

    [![請求の転記ページの売上税ボタン](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. **一時的な売上税トランザクション** ページで、計算の結果を確認します。 税金が計算されない場合は、[税金が計算されない、または税額がゼロ](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md) を参照してください。

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>すべての転記済売上税での TaxTrans レコードの検索

1. **税** \> **照会およびレポート** \> **売上税の照会** > **転記済売上税** の順に移動します。
2. **伝票** 列のヘッダーで、フィルター記号を選択して **TaxTrans** レコードを検索します。
3. 探している売上税レコードが見つかった場合は、日付を確認します。 日付が仕訳帳ヘッダーの日付と異なる場合は、追加のサポートを求める Microsoft サービス要求を作成します。

    [![転記済売上税ページ](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>詳細を確認するためにデバッグする

1. **TmpTaxWorkTrans** と **TaxUncommitted** が正しく生成されているかどうかをデバッグして決定する方法については、[TaxTrans のフィールド値が正しくない](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md) を参照してください。
2. **TaxTmpWorkTrans** または **TaxUncommitted** が正しく生成されている場合は、**TaxPost::SaveAndPost()** および **Tax::SaveAndPost** でブレークポイントを追加して、**TaxTrans** が挿入されない理由をデバッグします。

    [![コードに追加されたブレークポイント](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![追加されたブレークポイントの結果](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>カスタマイズが存在するかどうかの確認

前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。 カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

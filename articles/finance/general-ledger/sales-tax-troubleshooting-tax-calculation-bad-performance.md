---
title: 税計算のパフォーマンスがトランザクションに与える影響
description: このトピックでは、税計算のパフォーマンスおよびトランザクションに対する影響に関するトラブルシューティングの情報を提供します。
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: da19a83945450c2d35f95be2241b84e407860fe7808ff83934686ca2e00859bc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748957"
---
# <a name="tax-calculation-performance-affects-transactions"></a>税計算のパフォーマンスがトランザクションに与える影響

[!include [banner](../includes/banner.md)]

トランザクションは、税計算で発生するパフォーマンスの問題によって影響を受ける場合があります。 この問題のトラブルシューティングを行う場合は、必要に応じて次のセクションの手順に従います。

## <a name="review-the-transaction-line-count"></a>トランザクション明細行の数の確認

トランザクション明細行の数が多くないか (数百行以上など) を確認します。 多くない場合には、次のセクションに進みます。 トランザクションに数百行の明細行がある場合は、税計算を遅延させます。 詳細については、[仕訳帳の税金計算遅延の有効化](enable-delayed-tax-calculation.md)を参照してください。 

次に、次の条件が満たされているかどうかを確認できます。

- 大きなファイルからのインポート トランザクションが存在します。
- 複数のセッションで、同じ取引税計算を同時に処理します。
- トランザクションには複数の明細行が作成され、ビューはリアルタイムで更新されます。 たとえば、**一般仕訳帳** ページの **計算上の消費税金額** フィールドは、明細行のフィールドが変更された場合にリアルタイムで更新されます。

   [![仕訳伝票ページの計算上の消費税金額フィールド。](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

これらの条件が満たされている場合は、税計算を遅延させます。

## <a name="review-the-call-stack"></a>コール スタックの確認

コール スタックを確認して、税計算が複数回呼び出されるかどうかを確認します。 呼び出されない場合には、次のセクションに進みます。 コール スタックが複数回呼び出される場合は、次の手順に従って税計算時間を短縮します。

1. 仕訳帳でトランザクションが考慮される場合は、税計算を遅延させます。 詳細については、[仕訳帳の税金計算遅延の有効化](enable-delayed-tax-calculation.md)を参照してください。
2. トランザクションが発注書で、アプリケーション バージョンが 10.0.15 以降の場合、**PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** のフライティングを有効にして、税計算を最終計算まで遅延できます。

## <a name="review-the-call-stack-timeline"></a>コール スタック タイムラインの確認

コール スタック タイムラインを確認して、次の問題が存在するかどうかを識別します。 問題が発生している場合、**TaxUncommittedDoIsolateScopeFlighting** のフライティングを有効にして、問題を修正します。

- トランザクションにより、システムはセッションが終了するまで応答を停止します。 そのため、トランザクションで税の結果を計算できません。 次の図は、表示される「セッション終了」メッセージ ボックスを示しています。

    [![セッション終了メッセージ。](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- **TaxUncommitted** メソッドは、他のメソッドより時間がかかります。 たとえば、次の図では、**TaxUncommitted::updateTaxUncommitted()** メソッドの所要時間は 43,347.42 秒ですが、他のメソッドの所要時間は 0.09 秒です。

    [![メソッドの期間。](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>税計算のカスタマイズと呼び出し

カスタマイズする場合は、各行の **insert()** または **update()** メソッドで税計算を呼び出しません。 税計算をトランザクション レベルで呼び出す必要があります。

## <a name="determine-whether-customization-exists"></a>カスタマイズが存在するかどうかの確認

前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。 カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

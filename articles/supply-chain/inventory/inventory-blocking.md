---
title: 在庫ブロック
description: このトピックでは、Supply Chain Management の品質検査プロセスの一部である在庫ブロックの概要を示します。 在庫ブロックは、品目が処理または消費されるのを防ぐために使用できます。
author: yufeihuang
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b6169362c9e8cb3a9ace2f300dd9d80aa9cd085
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568882"
---
# <a name="inventory-blocking"></a>在庫ブロック

[!include [banner](../includes/banner.md)]

このトピックでは、Supply Chain Management の品質検査プロセスの一部である在庫ブロックの概要を示します。 在庫ブロックは、品目が処理または消費されるのを防ぐために使用できます。

在庫品目は、次の方法でブロックできます。

- 手動
- 品質指示を作成して
- 品質指示を生成するプロセスを使用して
- 在庫状態ブロックを使用

## <a name="blocking-items-manually"></a>手動での品目のブロック

**在庫ブロック** ページでトランザクションを作成することで、品目の数量をブロックできます。 手動でブロックできるのは、手持在庫として使用可能な品目のみです。 数量を手動でブロックする場合は、計画を行う際に、入庫予定を予定手持数量として含めるかどうか決める必要があります。 入庫予定とは、検査の完了後に手持在庫として使用可能になる予定の、ブロックされた品目です。 予定日は変更できます。 既定では、品質指示によってブロックされている品目について、**入庫予定** オプションが選択されます。 手動でブロックした数量は、**在庫ブロック** ページでトランザクションを削除することにより、キャンセルできます。

## <a name="blocking-items-by-creating-a-quality-order"></a>品質指示の作成による品目のブロック

**品質指示** ページの品質指示の作成によって確認する必要がある品目を指定できます。 品質指示を作成すると、指定する品目の数量がブロックされます。 品質指示に関連付けられるサンプリング計画は、検査する必要のある項目の数量のみを制御します。ブロックする数量ではありません。 品質指示に入力される品目の数量は、ブロックされる数量になります。サンプリング計画で検査に送るように指定する数量とは無関係です。

> [!NOTE]
> マスター プランでは、バッチの有効期限とブロックの在庫ステータス機能の使用はサポートされていません。 その結果、マスター プラン中に手持在庫が二重に除外される可能性があります。 期限切れバッチのブロックについては、在庫ステータスではなくバッチ状態コードの利用をお勧めします。

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>品質指示を生成するプロセスによる品目のブロック

品質プロセス中で品目が検査必要となっている場合、その品目の数量が自動的にブロックされます。 したがって、品質指示が自動的に生成されると、品質指示に関連付けられている品目サンプリング計画によって、ブロックする品目の数量と、検査する品目の数量の両方が制御されます。 **品目サンプリング** ページの **完全ブロック** オプションがオンの場合は、たとえば、購買注文明細行について、その全数量が検査中にブロックされます。品目のサンプリング数量には関係しません。

### <a name="example"></a>例

次の例では、発注書の梱包明細が転記されると、品質指示が生成されます。 **品質関連** ページでは、発注書の梱包明細の転記処理が、品質指示を有効にするプロセスとして指定してあります。

|段取り |ユーザー アクション |結果 |
|----|---|---|
| 品質関連によって、発注書の梱包明細が転記されたときに、品質指示が生成される必要のあることが指定されます。 品質指示の品目サンプリング設定によって、購買注文明細行の数量の 10% を検査しなければならないことが指定されます。 さらに、品目サンプリング設定で **完全ブロック** オプションが選択されているため、検査に送られる数量とは関係なく、購買注文明細行の全数量を検査中にブロックする必要があります。 | 梱包明細を転記します。 | 品質指示が生成されます。 品目の発注書数量の 10% が検査に送られます。 購買注文明細行の全数量がブロックされます。 |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>在庫状態ブロックを使用した品目のブロック

**在庫状態** ページの **在庫ブロック** パラメータを使用すると、どの在庫状態をブロック状態にするか指定できます。 在庫ステータスは、製造オーダー、販売注文、移動オーダー、出荷トランザクション、およびプロジェクト統合のブロック状態としては使用できません。 出荷作業の場合、使用可能な在庫状態の品目を使用します。 **破損** の状態の品目があり、マスター プランがこれらの品目で実行している場合、品目は存在しない見なされ、棚卸資産は自動的に補充されます。

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>在庫状態ブロックと品質指示ブロックの両方を使用する品目をブロックする場合は注意が必要です

**在庫ブロック** パラメーターが有効になっている在庫状態のを持つ在庫に関連付けられた品質指示を作成できます。 この場合、品質指示は、在庫状態によって作成されたものに加えて、追加の在庫ブロック レコードを生成します。 品質指示の在庫ブロックではパラメーター **入庫予定** が有効になります。これにより、在庫状態によりブロックされる追加の *注文済在庫* トランザクションが生成されます。 この組み合わせは、ブロックされた合計数量が手持の合計数量を超えているように見えるため、生成される在庫トランザクションの意味を理解するのが困難になります。 たとえば、1 個をサンプリングするために生成された品質指示を含む品目 A0001 10 個の入庫例でトランザクションを調べてみましょう。 この動作は、**在庫および倉庫管理パラメーター** ページでオプション **注文済品目の引当** が有効になっているかどうかにも依存します。

>[!NOTE]
>在庫状態ブロックと品質指示をまとめて使用する場合は、**注文済品目の引当** オプションを有効にしておくことを強くお勧めします。

### <a name="example-with-reserve-ordered-items-enabled"></a>「注文済品目の引当」が有効になっている例

**注文済品目の引当** を有効にすると、すべての在庫ブロック トランザクションは *引当済現物* または *引当済注文* のいずれかの状態になります。

| 在庫トランザクションの参照 | 受信 | 出庫 | 件数 | サイト | 倉庫 | 在庫状態 | 保管場所 | ライセンス プレート | コメント |
|---|---|---|---|---|---|---|---|---|---|
| 発注書 | 購買済 | | 10 個 | 2 | 24 | ブロック | RECV | receiptLp1 | | 
| 在庫ブロック | | 引当済現物 | -9 個 | 2 | 24 | ブロック | | | 在庫状態ブロックにより生成されたトランザクション |
| 在庫ブロック | | 引当済現物 | -1 個 | 2 | 24 | ブロック | RECV | receiptLp1 | 品質指示サンプリング ブロックによって生成されたトランザクション |
| 在庫ブロック | 発行済 | | 1 個 | 2 | 24 | ブロック | RECV | receiptLp1 | 品質指示サンプリング ブロックからの入庫予定 |
| 在庫ブロック | | 引当済注文 | 1 個 | 2 | 24 | ブロック | | | 在庫状態ブロックにより生成されたトランザクション

### <a name="example-with-reserve-ordered-items-disabled"></a>「注文済品目の引当」が無効になっている例

**注文済品目の引当** を無効にすると、それらの状態は *注文済* であるため、入庫予定を引当することはできません。そのため一部のブロックは *注文中* の状態のままになります。

| 在庫トランザクションの参照 | 受信 | 出庫 | 件数 | サイト | 倉庫 | 在庫状態 | 保管場所 | ライセンス プレート | コメント |
|---|---|---|---|---|---|---|---|---|---|
| 発注書 | 購買済 | | 10 個 | 2 | 24 | ブロック | RECV | receiptLp1 | |
| 在庫ブロック | | 引当済現物 | -9 個 | 2 | 24 | ブロック | | | 在庫状態ブロックにより生成されたトランザクション |
| 在庫ブロック | | 引当済現物 | -1 個 | 2 | 24 | ブロック | RECV | receiptLp1 | 品質指示サンプリング ブロックによって生成されたトランザクション |
| 在庫ブロック | 発行済 | | 1 個 | 2 | 24 | ブロック | RECV | receiptLp1 | 品質指示サンプリング ブロックからの入庫予定 |
| 在庫ブロック | | 受注中 | 1 個 | 2 | 24 | ブロック | RECV | receiptLp1 | 在庫状態ブロックにより生成されたトランザクション

2 つのケース間のトランザクション状態と分析コードの違いに注意してください。 このため、**注文済品目の引当** オプションを有効にすることをお勧めします。

<!-- KFM: (Enable this section when the feature leaves private preview)

### Disable expected receipts from quality orders that sample blocked inventory feature

To simplify the inventory transactions in the case of quality orders that sample inventory blocked as a consequence of inventory status, the system provides a feature that disables expected receipts from such quality orders. As the expected receipt is in any case immediately blocked by inventory status blocking, there is no reduction of on-hand inventory because of this change.

-->

## <a name="additional-resources"></a>追加リソース

[在庫ブロックの作成および管理](tasks/create-maintain-inventory-blocking.md)

[品質管理プロセス](quality-management-processes.md)

[商品の品質の調査](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
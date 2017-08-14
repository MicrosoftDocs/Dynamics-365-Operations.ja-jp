---
title: "在庫ブロック"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition の品質検査プロセスの一部である在庫ブロックの概要を示します。 在庫ブロックは、品目が処理または消費されるのを防ぐために使用できます。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7d00aaa272de32d4ef2082bf1822125800ca8a1e
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---

# <a name="inventory-blocking"></a>在庫ブロック

[!include[banner](../includes/banner.md)]


この記事は、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition の品質検査プロセスの一部である在庫ブロックの概要を示します。 在庫ブロックは、品目が処理または消費されるのを防ぐために使用できます。

在庫品目は、次の方法でブロックできます。
-   手動
-   品質指示を作成して
-   品質指示を生成するプロセスを使用して
-   在庫状態ブロックを使用

## <a name="blocking-items-manually"></a>手動での品目のブロック
**在庫ブロック** ページでトランザクションを作成することで、品目の数量をブロックできます。 手動でブロックできるのは、手持在庫として使用可能な品目のみです。 数量を手動でブロックする場合は、計画を行う際に、入庫予定を予定手持数量として含めるかどうか決める必要があります。 入庫予定とは、検査の完了後に手持在庫として使用可能になる予定の、ブロックされた品目です。 予定日は変更できます。 既定では、品質指示によってブロックされている品目について、**入庫予定**オプションが選択されます。 手動でブロックした数量は、**在庫ブロック** ページでトランザクションを削除することにより、キャンセルできます。

## <a name="blocking-items-by-creating-a-quality-order"></a>品質指示の作成による品目のブロック
**品質指示**ページの品質指示の作成によって確認する必要がある品目を指定できます。 品質指示を作成すると、指定する品目の数量がブロックされます。 品質指示に関連付けられるサンプリング計画は、検査する必要のある項目の数量のみを制御します。ブロックする数量ではありません。 品質指示に入力される品目の数量は、ブロックされる数量になります。サンプリング計画で検査に送るように指定する数量とは無関係です。

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>品質指示を生成するプロセスによる品目のブロック
品質プロセス中で品目が検査必要となっている場合、その品目の数量が自動的にブロックされます。 したがって、品質指示が自動的に生成されると、品質指示に関連付けられている品目サンプリング計画によって、ブロックする品目の数量と、検査する品目の数量の両方が制御されます。 **品目サンプリング** ページの**完全ブロック** オプションがオンの場合は、たとえば、購買注文明細行について、その全数量が検査中にブロックされます。品目のサンプリング数量には関係しません。
### <a name="example"></a>例

次の例では、発注書の梱包明細が転記されると、品質指示が生成されます。 **品質関連**ページでは、発注書の梱包明細の転記処理が、品質指示を有効にするプロセスとして指定してあります。

|段取り                                                                     |ユーザー アクション                 |結果             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| 品質関連によって、発注書の梱包明細が転記されたときに、品質指示が生成される必要のあることが指定されます。 品質指示の品目サンプリング設定によって、購買注文明細行の数量の 10% を検査しなければならないことが指定されます。 さらに、品目サンプリング設定で**完全ブロック** オプションが選択されているため、検査に送られる数量とは関係なく、購買注文明細行の全数量を検査中にブロックする必要があります。 | 梱包明細を転記します。 | 品質指示が生成されます。 品目の発注書数量の 10% が検査に送られます。 購買注文明細行の全数量がブロックされます。 |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>在庫状態ブロックを使用した品目のブロック
**在庫状態**ページの**在庫ブロック**パラメータを使用すると、どの在庫状態をブロック状態にするか指定できます。 在庫ステータスは、製造オーダー、販売注文、移動オーダー、出荷トランザクション、およびプロジェクト統合のブロック状態としては使用できません。 出荷作業の場合、使用可能な在庫状態の品目を使用します。 **破損**の状態の品目があり、マスター プランがこれらの品目で実行している場合、品目は存在しない見なされ、棚卸資産は自動的に補充されます。



<a name="see-also"></a>参照
--------

[在庫ブロックの作成および管理 (タスク ガイド)](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-maintain-inventory-blocking)

[品質管理プロセス](quality-management-processes.md)

[商品の品質の調査 (タスク ガイド)](/dynamics365/unified-operations/supply-chain/inventory/tasks/inspect-quality-goods)





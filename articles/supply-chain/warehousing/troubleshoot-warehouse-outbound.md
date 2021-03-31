---
title: 出庫倉庫操作のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での出庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1344a1c16bf72b31f7aaf18aaeb6e08c7bc9d87e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223269"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>出庫倉庫操作のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management での出庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>エラー メッセージ "販売注文をリリースできませんでした" が表示されます。

### <a name="issue-description"></a>問題の説明

この問題は、いくつかの理由で発生する可能性があります。 たとえば、与信管理保留中の注文で、販売注文に関連付けられているすべての販売明細行に有効な住所が入力されるまで出荷を作成することはできません。 また、注文を倉庫にリリースする前に対応する必要がある注文保留もあります。 この保留は注文固有の場合もありますが、顧客 ID に含まれている場合もあります。

### <a name="issue-resolution"></a>問題の解決

販売注文と注文明細行の住所を追加または更新し、注文を倉庫にリリースします。 注文は、有効な配送先住所がある場合にのみ倉庫にリリースできます (**組織管理** モジュールでの住所形式の設定に従って)。

注文の保留を調査し、問題に対処します。 次に、注文または顧客から保留を削除し、注文を倉庫に解放します。

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>メッセージ "積荷 1% の出荷が確認されました" が表示されます。 ただし、明細行は転記されません。

### <a name="issue-description"></a>問題の説明

積荷の出荷が確認されましたが、それ以上転記は行われませんでした。

### <a name="issue-resolution"></a>問題の解決

出荷確認は転記に影響しません。 出荷と積荷のステータスが更新されるだけです。 転記は、別のプロセスで行われる必要があります。

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>エラー メッセージ "倉庫管理が有効になっているため、倉庫 1% に対して直納を処理できません。 倉庫管理で有効になっていない別の倉庫を指定してください" が表示されます。

### <a name="issue-description"></a>問題の説明

倉庫管理 (WMS) が有効になっている倉庫から直送するための品目が販売明細行に追加されます。 販売明細行が更新されると、このエラー メッセージが表示されます。 

### <a name="issue-resolution"></a>問題の解決

Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。 現時点では、WMS は直接配送をサポートしていません。 したがって、直納を使用するには、WMS 以外の品目および倉庫を選択する必要があります。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
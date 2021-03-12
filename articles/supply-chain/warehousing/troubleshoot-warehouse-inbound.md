---
title: 入庫倉庫操作のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での入庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。
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
ms.openlocfilehash: 71f590ec01b757de298bd2692fdbdb0324843376
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970254"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>入庫倉庫操作のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management での入庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>エラー メッセージ "品質指示 %1 が生成されました。 クラスター プロファイルが見つかりませんでした。コンフィギュレーションを確認してください" が表示されます。

### <a name="issue-description"></a>問題の説明

このエラー メッセージは、品質管理 (QMS) が有効になっている入庫プロセスに関連しています。 環境内のコンフィギュレーションによっては、エラー メッセージを生成するトランザクションに関する詳細情報を追加すると、問題を修正できる場合があります。

### <a name="issue-resolution"></a>問題の解決

最初に、[クラスター ピッキング](set-up-cluster-picking.md)設定を確認し、クラスター プロファイルが正しく設定されていることを確認します。 クラスター プロファイルが設定されていない場合は、モバイル デバイスのメニュー項目をクラスター ピッキングに使用することはできません。 環境によっては、その他の関連するコンフィギュレーションも検討する必要があります。

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>混合ライセンス プレートの受取は、貸方を除く廃棄コードに対しては機能しません。

### <a name="issue-description"></a>問題の説明

廃棄コードの **アクション** フィールドが *貸方* または *仕損* に設定されている場合、返品品目を処理するには、[混合ライセンス プレートの受取](mixed-license-plate-receiving.md) メニュー項目のみ使用できます。

### <a name="issue-resolution"></a>問題の解決

Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。 現在のところ、**アクション** フィールドが *貸方* または *仕損* に設定された[廃棄コード](../service-management/set-up-disposition-codes.md)のみが、混合ライセンス プレート受取でサポートされています。

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>製品受領書の更新の定期処理タスクを実行すると、未確認の発注書が確認されます。

### <a name="issue-description"></a>問題の説明

*製品受領書の更新* 定期タスクを実行すると、*登録済* の在庫トランザクション ステータスがある未確認の発注書が自動的に確認されます。

### <a name="issue-resolution"></a>問題の解決

新しい入庫積荷処理機能 *積荷数量の受入超過* によってこの問題が修正されます。 この機能を有効にするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)に移動して、次の機能を (記載されている順序で) オンにします。

1. 購買注文在庫トランザクションを積荷に関連付けます
1. 積荷数量の過剰入荷

詳細については、[発注書に対する登録済製品の数量の転記](inbound-load-handling.md#post-registered-quantities)を参照してください。

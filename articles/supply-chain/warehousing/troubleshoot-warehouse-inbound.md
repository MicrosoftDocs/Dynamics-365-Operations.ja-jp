---
title: 入庫倉庫操作のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での入庫倉庫操作の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6d7fcb2ed32c57b8701bee5b90889a0a63e1f7061aa9014480ae8c543e1f229a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748670"
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

新しい入庫積荷処理機能 *積荷数量の受入超過* によってこの問題が修正されます。 この機能を有効にするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースに移動して、次の機能を (記載されている順序で) オンにします。

1. 購買注文在庫トランザクションを積荷に関連付けます
1. 積荷数量の過剰入荷

詳細については、[発注書に対する登録済製品の数量の転記](inbound-load-handling.md#post-registered-quantities)を参照してください。

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a>入庫注文を登録すると、"数量が有効ではありません" というエラー メッセージが表示されます。

### <a name="issue-description"></a>問題の説明

**ライセンス ユーザー グループ化ポリシー** フィールドが、着信注文の登録に使用されるモバイル デバイス メニュー項目に対して *ユーザー定義* に設定されている場合は、エラー メッセージ ("数量が有効ではありません") が表示され、登録を完了できません。

### <a name="issue-cause"></a>問題の原因

*ユーザー定義* がライセンス プレートのグループ化ポリシーとして使用されている場合、単位シーケンス グループによって示される別のライセンス 契約で、受信する在庫が別のライセンス 契約に 分割されます。 受け取る品目を追跡するためにバッチ番号またはシリアル番号を使用する場合は、登録されたライセンス プレートごとに、各バッチまたはシリアルの数量を指定する必要があります。 ライセンス プレートで指定された数量が、現在の分析コードに対してまだ受け取る必要がある数量を超えている場合は、エラー メッセージが表示されます。

### <a name="issue-resolution"></a>問題の解決

モバイル デバイス メニュー項目を使用して品目を登録する場合、**ライセンス プレートのグループ化ポリシー** フィールドが *ユーザー定義* に設定されている場合は、ライセンスの承認番号、バッチ番号、またはシリアル番号の確認または入力をシステムで要求する場合があります。

ライセンス契約の確認ページには、現在のライセンス 契約に割り当てられている数量が表示されます。 バッチまたはシリアルの確認ページには、現在のライセンス 契約で引き続き受け取る必要がある数量が表示されます。 ライセンスプレートとバッチまたはシリアル番号の組み合わせに対して登録する数量を入力できるフィールドも含まれます。 この場合、ライセンスプレートに登録されている数量が、まだ受け取る必要がある数量を超えないようにしてください。

また、受信注文の登録でライセンスが多数生成されている場合は、**ライセンス プレートのグループ化ポリシー** フィールドの値を *ライセンス プレートのグループ化* に変更したり、品目に新しい単位シーケンス グループを割り当てたり、単位シーケンスグループの **ライセンス プレートのグループ化** オプションを無効にすることもできます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

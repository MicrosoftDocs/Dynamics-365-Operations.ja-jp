---
title: バッチ ジョブからの出荷の確認
description: この記事では、出荷準備が完了した積荷の出荷移動オーダー出荷を自動的に確認するバッチ ジョブの設定方法について説明します。
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875104"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>バッチ ジョブからの出荷の確認

[!include [banner](../includes/banner.md)]

この記事では、出荷準備が完了した積荷の出荷移動オーダー出荷を自動的に確認するバッチ ジョブの設定方法について説明します。 ここで説明するバッチジョブは、販売注文に対してではなく、転送注文の出荷にのみ適用されます。

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>バッチジョブからの出荷を確認する機能のオン/オフを切り替える

この記事で説明する機能を使用するには、ご利用のシステムで *バッチ ジョブからの出荷を確認する* 機能がオンになっている必要があります。 Supply Chain Management のバージョン 10.0.21 では、この機能は既定で有効になっています。 Supply Chain Management 10.0.25 では、この機能は必須なため、オフにすることはできません。 10.0.25 より前のバージョンを使用している場合、管理者は [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *バッチジョブからの出荷を確認する* 機能を検索して、この機能のオン/オフを切り替えることができます。

## <a name="process-outbound-shipments"></a>出荷の処理

出荷の準備ができている積荷に対して、出荷確認の実行をスケジュール設定したバッチジョブを設定するには、次の操作を行います :

1. **倉庫管理 \> 定期タスクは \> 出荷を処理する** に移動します。
1. **出荷の確認** ダイアログ ボックスが開きます。 **対象に含めるレコード** クイック タブで、**フィルター** を選択します。
1. クエリ エディター ダイアログボックスが開きます。 **範囲** タブで、新しい行を追加して以下の値を設定します :
    - **テーブル** - *積荷*
    - **派生テーブル** - *積荷*
    - **フィールド** - *積荷の状態*
    - **基準** - *積荷済*
1. **OK** を選択して、**出荷確認** ダイアログ ボックスに戻ります。
1. **バックグラウンドで実行** クイックタブで、**バッチ処理** を **はい** に設定します。
1. **バックグラウンドで実行** クイックタブで、**繰り返し** を選択します。
1. **繰り返しの定義** ダイアログ ボックスが開きます。 業務の要件に応じて実行スケジュールを設定します。
1. **OK** を選択して、**出荷確認** ダイアログ ボックスに戻ります。
1. **出荷の確認** ダイアログ ボックスの **OK** を選択し、バッチ ジョブをバッチキューに追加します。

詳細については、[バッチ処理の概要](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
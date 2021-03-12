---
title: バッチ ジョブからの出荷の確認
description: このトピックでは、出荷準備が完了した転送注文を自動的に確認するバッチ ジョブの設定方法について説明します。
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 48257967ce360b1d4969124411d5976b807bf9e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996304"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>バッチ ジョブからの出荷の確認

[!include [banner](../includes/banner.md)]

このトピックでは、出荷準備が完了した転送注文を自動的に確認するバッチ ジョブの設定方法について説明します。 ここで説明するバッチジョブは、販売注文に対してではなく、転送注文の出荷にのみ適用されます。

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>バッチジョブからの出荷確認機能を有効にする

この機能を使用する前に、システム上で有効にする必要があります。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ページで機能状態を確認し、必要に応じて有効化することができます。 この機能は次のように一覧表示されます :

- **モジュール** - *倉庫管理*
- **機能名** - *バッチジョブから出荷を確認する*

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

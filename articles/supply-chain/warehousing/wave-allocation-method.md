---
title: サイクル配賦
description: このトピックでは、サイクル配賦の手順を設定して構成する方法と、それの並列処理を可能にする方法について説明します。
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: feee33a7d4ea3f0d9c4d671210293a28aac14f61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823170"
---
# <a name="wave-allocation"></a>サイクル配賦

[!include [banner](../includes/banner.md)]

サイクルの処理は時間がかかる可能性があり、処理時間のほとんどは配賦ステップと作業作成ステップに費やされます。

これらの各ステップを並列して実行することが可能になりました。これはサイクル処理のパフォーマンスを改善し、同じ倉庫でサイクルのスループットをより大きくすることを可能にします。 このトピックでは、サイクル配賦手順を並列して実行するために設定する方法について説明します。 並列して実行する作業作成の設定方法の詳細については、[サイクル中に作業作成をスケジュールする](configure-wave-schedule-work-creation.md) を参照してください。

以前は、倉庫につき一度に配賦できるサイクルは 1 つのみでした。 この制約が削除され、品目と分析コードが予約階層の場所より上にある場所のみをロックする新しい制約に置き換えられました。 場所の上の分析コードには、常に製品分析コードが含まれます。 たとえば、品目が *色* を使用して構成されている場合は、*赤*、*青*、*黄色* はそれぞれバリアントを並列処理できます。

つまり、その場所の上に同じ分析コードを持つ同じ品目を 1 つ多く割り当てると、同じ品目および分析コードに対するロックを取得するまで待つ必要があります。 ロックを時間的に取得できない場合はエラーが発生し、その場合は処理に失敗します。

並行処理を使用するには、複数のジョブをバッチで実行する必要があります。

## <a name="performance-improvements"></a>パフォーマンスの向上

並行処理のパフォーマンス上の利点は、次の 2 つのカテゴリに分類されます。

- **スループットの向上** -  : 並行処理が行なくても、特にサイクル内で品目が重複しない場合など、並行処理でデータが構成されなくても、スループットが向上するのが一般的です。
- **単一サイクルの配賦の改善** - 並行配賦に切り替えてから顧客データをテストすることにより、50% 近いパフォーマンスの向上が示されました。 並行処理は場所の上の品目および分析コードごとに行われるので、その改善は 1 つの場所に含まれるさまざまな品目の数、使用可能なインフラストラクチャ、配賦の期間と作業作成の期間に依存します。

## <a name="configure-parallel-allocation"></a>並列配賦の構成

### <a name="warehouse-management-parameters"></a>倉庫管理パラメーター

並行配賦処理を使用するには、**倉庫管理 > 設定 > 倉庫管理パラメータ** に移動して、**サイクル処理** タブを開いて、次の設定を行います。

- **サイクル処理バッチ グループ** - サイクルの初期処理で使用するバッチ グループを選択します。 後続の配賦の処理は、異なるバッチ グループを使用して行います。
- **バッチでサイクルを処理する** - 並行処理を使用するにはこれを *はい* に設定します。
- **ロックを待機 (ミリ秒)** - 配賦ステップが、他の配賦ステップでロックされたシステム リソースを待機する時間を、ミリ秒単位で入力します。 この時間を超えた場合、ウェーブは処理されず、エラー メッセージが表示されます。 1 つの論理ユニットの配賦を終了させるのに、少なくとも数秒を許可することをお勧めします。

**倉庫管理パラメータ** ページのこれらのオプションとその他の調整処理オプションの詳細については、[サイクル処理の 倉庫パラメータ](wave-warehouse-parameters.md) を参照してください。

## <a name="wave-process-methods"></a>ウェーブのプロセス方法

並行処理を設定するには、次をおこないます。

1. **倉庫管理 > 設定 > サイクル > サイクル処理のメソッド** に移動します。
1. グリッドで `allocateWave`メソッドを選択します。
1. アクション ペインで、**タスクの作成** を選択します。
1. **サイクル投稿メソッドの構成** ページが開きます。 このグリッドには、`allocateWave` メソッドを構成した各倉庫が一覧表示されます。 並列処理は、一覧表示されている倉庫に対してのみ使用されます。 アクション ペインのボタンを使用して、必要に応じて倉庫をグリッドに追加したり、グリッドから倉庫を削除したりします。 
1. 各倉庫について、次の設定を行います。
    - **バッチ タスクの最大数** - 選択した倉庫の配賦に使用するバッチ タスクの数を指定します。 最適なバッチ タスクの数は、使用可能なインフラストラクチャと、サーバーで処理されている他のバッチ ジョブによって異なります。 その結果、8 つのタスクを使用して優れた結果が得られた、という 4 つのコア環境でのテストが示されました。
    - **サイクル処理バッチ グループ** - 特定のバッチ グループを複数の倉庫に対して使用すると、配賦処理を倉庫ごとにスケールアウトできます。

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>すべての法人エンティティ間での並列処理の有効化または無効化

すべての法人にまたがって並列で実行する `allocateWave` メソッドを設定することをお勧めします。なぜならこのメソッドはサイクル処理のパフォーマンスを改善するのに役立ちます。 Supply Chain Management のバージョン 10.0.17 から、新しいインストールおよび更新されたシステムすべてで、*サイクル配賦メソッドのサイクル並列処理* 機能が規定で有効になっていて、再度オフにすることはできません。 この機能を有効にすると、次のようになります。

- この `allocateWave` メソッドが更新され、並行処理の数と同じ、同時に実行されるタスクの数を実行できる **サイクル処理メソッド** ページを使用して、タスク構成設定が含まれます。 その結果、各工程で使用される時間 (一般に総処理時間の 30% ~ 60%) から、タスクの数と大まかに等しい係数が減らされます。 これらのタスクを処理するために割り当てられるバッチを選択することもできます。 すべての法人が、一括してサイクルを処理するように構成される点に注意が必要です。 既にバッチのサイクル処理をするように構成されている倉庫と、その `allocateWave` メソッドを並列して使用するように構成されている倉庫については、既存の構成が維持されます。
- 既定では、すべての新しい法人がバッチのサイクルを処理するように構成されています。 **倉庫管理プロセス** オプションが有効になっているすべての新しい倉庫に、既定で並列で `allocateWave` メソッドを実行するように構成されます。
- **倉庫管理パラメータ** ページジで、**バッチに保存する** が *はい* に設定され、**ロックを待機 (ミリ秒)** が既定の 15 秒に設定されます。 つまり、すべてのサイクルがバッチで実行されます。 実行中のサイクルは、この配賦ステップで品目のロックと位置にある分析コードを取得します。 他のサイクル処理タスクが同じ特定のレコードのロックを取得しようとすると、現在の処理が終了するまでブロックされます。 **ロックを待機 (ミリ秒)** の設定により、システムがロックがリリースされる前に待機 する最大時間が設定されます。

並行配賦処理には、サイクル処理をバッチで実行する必要があります。 そのため、**バッチで保存されたプロセス** 設定をオフにすると、バッチ設定で保存されます。特に、関連するジョブ メソッドのタスク構成で定義された並行処理を使用している場合は、処理がバッチ設定に保存されます。

必要に応じて、*サイクルの配賦メソッドのサイクル並行処理* 機能が自動的に有効になっている場合は、既定で行われた各設定を元に戻すことができます。 これを行うには、次の手順を実行します。

- **倉庫管理\>設定\> 倉庫管理パラメーター** の順に移動します。 **制御処理** タブで、**バッチの処理** と **ロックを待機 (ミリ秒)** の値 を適用します 。
- **倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。 `allocateWave` メソッドを選択します。 アクション ペインで、**タスク構成** を選択して、メソッドが並列して実行するために設定されている各倉庫を一覧表示するページを開きます。 必要に応じて、バッチ タスクの数と、リストされている各倉庫に割り当てられている複数のグループを変更または削除します。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="troubleshoot-using-the-infolog"></a>情報ログを使用したトラブルシューティング

バッチ フレームワークが使用されている場合は、ファイル内で発生したエラーが、バッチ ジョブ情報ログの一部としてキャプチャされます。 サイクルに関連するバッチ ジョブを読み取るには、次の操作を行います。

1. **倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ** の順に移動します。
1. 検査するサイクルを選択します。
1. アクション ペインで、**サイクル** タブを開き、**サイクル** グループから、**バッチ ジョブ** を選択します。

プログラムによる処理はセルフ修正なので、処理中に検出されたエラーは情報ログを使用して報告する必要があります。

並行処理に関連する一般的なエラーは、2 つの波が同じ品目を同時に割り当てようとして、もう 1 つのジョブが完了しないので、指定した時間内にロックを取得できないという場合があります。 この状況が発生すると、バッチ ジョブ ログに、品目のロックを取得できなかったという通知が含まれるので、失敗したジョブを再度処理する必要があります。

処理が並行処理で発生している場合から、処理の状態を追跡するために、別のテーブルでデータを管理する必要があります。 つまり、バッチ ジョブのログにキー エラーの重複などのエラーが含まれる可能性があります。

バッチ タスクからのエラーは、バッチ ジョブ ログの一部です。 最も重要な情報は一般にボトムに表示されます。

たとえば、SQL 接続が終了した場合、バッチ ジョブが実行されているのように見えたが処理が停止されている不整合の状態で、クエリの処理が終了する可能性があります。 このようなサイクルは検出できないので、次の何を実行したら失敗した波をクリーンアップしようとします。 または、現在の何を示す値が不整合な状態の場合は、次の手順を実行します。

1. **倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ** の順に移動します。
1. クリーンアップする必要があるサイクルを選択します。
1. アクション ペインで、**サイクル** タブを開き、**サイクル** グループから、**サイクルデータのクリーンアップ** を選択します。

### <a name="troubleshoot-using-the-wave-progress-log"></a>進捗ログを使用したトラブルシューティング

**倉庫管理パラメータ** ページで **ファイルの処理状況ログの作成** オプションが有効になっている場合は、品目の配賦が開始および終了するごとにログ レコードが作成されます。 このログは、最初のテスト中やトラブルシューティング時など、必要な場合にのみ有効にしてください。 このオプションが有効な場合、次の手順を実行してログを表示できます。

1. **倉庫管理 \> 出庫ウェーブ \> 出荷ウェーブ \> すべてのウェーブ** の順に移動します。
1. 検査するサイクルを選択します。
1. アクション ペインの、**ウェーブ** タブの、**ウェーブ** グループで、**処理** を選択します。
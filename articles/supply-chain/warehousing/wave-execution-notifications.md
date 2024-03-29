---
title: ウェーブの実行通知
description: この記事では、ウェーブの実行通知についての説明と、設定方法について解説します。
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: a6a554965c11eea3b4fa53fe4dbc4bac04624026
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336578"
---
# <a name="wave-execution-notifications"></a>ウェーブの実行通知

[!include [banner](../includes/banner.md)]

*ウェーブの実行通知* 機能は、ビジネス イベントとアクション センターを使用して、ウェーブの実行に関する通知を配信します。 通知を生成するイベントのタイプや倉庫、および通知を受信するユーザーを指定できます。

ナビゲーション バーの右側にある **メッセージを表示** ボタン (ベルの記号) は、現在のユーザーにアクション センター メッセージが表示される日を示します。 ユーザーは、**メッセージの表示** ボタンを選択してアクション センターを開き、メッセージを確認できます。

ビジネス プロセスの実行時に、ビジネス イベントが発生します。 業務プロセスはタスクで構成されます。 ビジネス プロセス中には、それに参加するユーザーは、タスクを完了するビジネス アクションを実行します。 ビジネス イベントは外部システムが財務と運用アプリケーションから通知を受信するメカニズムを提供します。 これにより、システムは、ビジネス イベントに対してビジネス アクションを実行できます。 詳細については、[ビジネス イベントの概要](../../fin-ops-core/dev-itpro/business-events/home-page.md)を参照してください。

## <a name="turn-the-wave-execution-notifications-feature-on-or-off"></a>ウェーブの実行通知機能のオン/オフを切り替える

この機能を使用するには、システムでオンにする必要があります。 Supply Chain Management バージョン 10.0.25 では、この機能は既定で有効になっています。 Supply Chain Management バージョン 10.0.29 では、この機能は必須であり、オフにすることはできません。 10.0.29 より以前のバージョンを使用している場合、管理者は [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *ウェーブの実行通知* 機能を検索して、この機能をオンまたはオフにすることができます。

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>シナリオ: アクション センターにウェーブのバッチ実行通知を送信する

このシナリオは、アクション センターを介して特定のロールにウェーブのバッチ実行エラーに関する通知を送信する、エンドツーエンドのフローについてです。

### <a name="make-demo-data-available"></a>デモ データを有効化する

このシナリオを実行するには、デモ データがインストールされている必要があり、法人として **USMF** を選択する必要があります。

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>ウェーブがバッチ モードで実行されるのを確認する

1. **倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。
1. **ウェーブの処理中** クイックタブで、**ウェーブのバッチ処理** オプションを *はい* に設定します。

> [!NOTE]
> ウェーブのバッチ実行通知を無効にする場合は、**ウェーブのバッチ処理通知** オプションを *はい* に設定します。

### <a name="configure-a-wave-notification-policy"></a>ウェーブの通知ポリシーの構成

ウェーブの通知ポリシーは、送信する通知のタイプと通知を受け取るユーザーを定義します。

1. **倉庫管理 \> 設定 \> ウェーブ \> ウェーブの通知ポリシー** に移動します。
1. 以下の設定をしたレコードを作成します:

    - **ウェーブの通知ポリシー:** *24BatchError*
    - **説明:** *倉庫 24 バッチ エラー*
    - **送信通知を有効にする:** *エラーのみ*
    - **ロール:** *システム管理者*

        > [!NOTE]
        > このシナリオではデモ データを使用するため、*システム管理者* ロールは、シンプルになるように選択されています。 したがって、システム管理者ユーザーとしてログインすると通知が表示されます。 ただし通常は、*倉庫マネージャー* など、特定のロールを選択して、ウェーブのバッチ実行エラーを通知する必要があります。

1. アクション ウィンドウで、**保存** を選択します。

### <a name="configure-a-wave-template"></a>ウェーブのテンプレートを構成する

ウェーブのテンプレートを使用すると、特定のウェーブ メソッドのインスタンスをこれに対応するウェーブ ラベルのテンプレートにリンクさせることができます。

1. **倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。
1. リスト ペインで、**ウェーブ テンプレート タイプ** フィールドを *出荷* に設定し、倉庫 24 の *24 出荷の既定* ウェーブ テンプレートを選択します。
1. **一般** クイックタブで、**ウェーブの通知ポリシー** フィールドを *24BatchError* に設定します。

### <a name="configure-a-work-template"></a>作業テンプレートを構成する

作業テンプレートは、作業を生成するために、ウェーブの実行中に使用されます。 このシナリオでは、ウェーブの実行がエラーを引き起こします。 作業テンプレート クエリに存在しない倉庫を設定すると、ウェーブの実行が失敗するため通知が送信されます。

1. **倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。
1. リスト ペインで、**作業テンプレート タイプ** フィールドを *販売注文* に設定し、倉庫 24 の *24 SO ステージ* 作業テンプレートを選択します。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. クエリ エディターのダイアログ ボックスにある **範囲** タブで、次の行を編集します (存在しない場合は追加します)。

    - **テーブル:** *一時的な作業トランザクション*
    - **派生テーブル:** *一時的な作業トランザクション*
    - **フィールド :** *倉庫*
    - **基準:** 値を *24* から *エラー* に変更します。

1. **OK** を選択して、変更を確認します。

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>販売注文を作成して倉庫にリリースする

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** に移動します。
1. 以下の設定で販売注文を作成します:

    - **顧客アカウント:** *US-001*
    - **倉庫:** *24*

1. **販売注文明細行** クイックタブで、次を設定されている販売注文の明細行を追加します。

    - **品目番号:** *A0001*
    - **数量:** *10*

    > [!NOTE]
    > これらの品目と数量は一例です。 指定された倉庫に十分な在庫が含まれている必要があります。

1. 新しい明細行が **販売注文明細行** クイック タブで選択されている間に、ツールバーで **在庫 \> 予約** の順に選択します。
1. **引当** ページのアクション ウィンドウで、**引当ロット** を選択します。 その後、ページを閉じます。
1. アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。

### <a name="notifications-from-wave-batch-job-execution"></a>ウェーブのバッチ ジョブ実行からの通知

ビジネス イベントの設定に応じて、ウェーブの実行失敗に関する通知が送信されます。 アクション センターからのメッセージは次の例のようになり、失敗したウェーブへのリンクが含まれます。

> **ウェーブ実行中のエラー**  
> ウェーブ USMF-000000001 を実行中にエラーが発生しました。  
> 最後のメッセージ: ウェーブ USMF-000000001 に必要な作業が作成されていません。
>
> **状態**  
> 有効
>
> ウェーブの詳細を開く

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


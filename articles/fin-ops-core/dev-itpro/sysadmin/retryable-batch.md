---
title: バッチ再試行の有効化
description: このトピックでは、障害が発生した場合にバッチ ジョブで自動再試行を有効にする方法について説明します。
author: matapg007
ms.date: 01/10/2022
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2021-05-31
ms.openlocfilehash: 175b111bf7f6728ad7b16ec72579c408093ecd1a
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645035"
---
# <a name="enable-batch-retries"></a>バッチ再試行の有効化

[!include [banner](../includes/banner.md)]

このトピックでは、財務と運用アプリのバッチ ジョブで再試行を実装する方法、および障害が発生した場合に自動再試行を有効にする方法について説明します。 現在、バッチ プラットフォームでは、バッチの弾力性を有効にして障害を回避するための 3 つの方法が提供されています。

## <a name="retry-the-batch-job-task-regardless-of-the-error-type"></a>エラー タイプにかかわらず、バッチ ジョブ タスクを再試行する

エラー タイプにかかわらず、バッチ ジョブ タスクを常に再試行する場合は、このオプションを使用をお勧めします。 **最大再試行回数** の値は、発生する例外のタイプにかかわらず、タスクに適用される再試行回数を指定します。 タスクが失敗した場合、バッチ プラットフォームは再試行された回数を評価します。 数字が **最大再試行回数** の値より小さい場合、タスクは準備完了状態に戻り、再び取得することができます。 

1. **バッチ ジョブ** ページで **バッチ タスクの表示** を選択します。
2. **一般** タブで **最大再試行回数** フィールドを設定します。

## <a name="retry-the-batch-job-task-when-transient-sql-server-errors-occur"></a>SQL Server の一時的なエラーが発生した場合にバッチ ジョブ タスクを再試行する

現在、財務と運用アプリにおける Microsoft SQL Server への接続が簡単に失われると、すべてのバッチ ジョブが失敗します。 この動作により業務プロセスが中断します。 クラウド サービスでは接続が失われることは避けられないので、Microsoft はこのタイプのエラーが発生した場合の自動再試行を有効にします。

既定では複数の実行の後でも、べき等であり同じ結果を生成する全てのバッチ クラスは再試行されます。 バッチ クラス インスタンスのべき等フラグを設定するには、**classinstance.BatchInfo().parmIdempotent(boolean)** を使用します。 

すべてのバッチ ジョブがべき等でない可能性もある (バッチでクレジット カード トランザクションを実行する場合など) ため、すべてのバッチ ジョブで再試行を等しく有効にすることはできません。 再試行を安全に有効にできるよう、Microsoft はバッチ ジョブにメタデータを追加して、自動的に再試行できるかどうか表示するようにしました。 バージョン 10.0.18 と 10.0.19 の間では、Microsoft バッチ ジョブの 90% 以上が明示的に **BatchRetryable** インターフェイスを実装し、**isretryable** 値は適切に設定されました。 **BatchRetryable** インターフェイスを実装していないすべてのジョブで、**isRetryable** の既定値は **False** です。

**BatchRetryable** インターフェイスが実装され、**isRetryable** が **True** に設定されているジョブに対してのみ再試行は有効になります。 この機能では、SQL Server 接続が中断した後に再試行が発生します。 Microsoft は引き続き、他の例外での再試行を追加します。

クラス評価の再試行可能フラグの優先順位は、**isIdempotent** フラグ、フラグ、バッチ クラス上書きコンフィギュレーション、および **isRetryable** フラグの順序です。 

1. もし **isIdempotent** フラグが **True** の場合は、他の 2 つのフラグに関係なくタスクが再試行されます。 
2. もし **isIdempotent** が **False** で、バッチ クラスの上書きコンフィギュレーションが **True** の場合、タスクは再試行されます。 もしバッチ クラスの上書きコンフィギュレーションが **False** の場合は、上書き値なのでタスクが再試行されません。
3. もし **isIdempotent** フラグが **False** でバッチ クラスの上書きコンフィギュレーションが実装されていない場合、**isRetryable** フラグが評価されます。 値が **True** の場合、タスクは再試行されます。 **False** の場合、タスクは再試行されません。

再試行の最大数と再試行間隔は、バッチ プラットフォームによって制御されます。 **BatchRetryable** インターフェイスは 5 秒後に開始し、間隔の時間が 5 分に達した後、再試行を停止します。 (間隔の時間は次のように増加します: 5、8、16、32 など。)

> [!NOTE]
> SQL の一時的エラーの場合、バッチ プラットフォームは、顧客クラスからスローされた例外が **TransientSqlConnectionError** タイプの例外であるか、**TransientSqlConnectionError** がカスタム例外内で入れ子になった例外として折り返されスローできる場合にタスクを再試行します。

## <a name="batch-odata-action-capability"></a>バッチ OData アクション機能

前の 2 つのオプションのように、このオプションは再試行を直接実行しません。 これにより、顧客はジョブを再トリガーする前にカスタム ロジックを追加できます。 ジョブの実行が失敗した場合は、対応するビジネス イベントをリッスンし、失敗を再試行できるかどうかを決定できます。 バッチ プラットフォームによって、バージョン 10.0.22 (プラットフォーム update 46 を含む) から新しい Open Data Protocol (OData) アクションが公開されました。 エンドポイントへの呼び出しでジョブ ID が指定された場合、ジョブは実行に対して再キューされます。

詳細については、[バッチ OData API](batch-odata-api.md) を参照してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="how-do-retries-work-for-my-custom-batch-jobs"></a>自分のカスタム バッチ ジョブの再試行を実行するにはどうしたらよいですか?

カスタム バッチ ジョブに変更はありません。 自動再試行を活用するには、カスタム バッチ ジョブで **BatchRetryable** インターフェイスを明示的に実装し、**isRetryable** を **true** に設定します。 安全に再試行できるようにバッチ ジョブを変更しなければならない場合があることに注意します。

### <a name="how-do-i-implement-the-retryable-interface"></a>再試行可能なインターフェイスをどのようにして実装しますか?

バッチ クラスに次のコードを追加します。

詳細については、[最終的な方法および Wrappable 属性](../extensibility/method-wrapping-coc.md) を参照してください。

```
//RunBaseBatch
class TestBatchJob extends RunBaseBatch implements BatchRetryable
{
    [Wrappable(true), Replaceable(true)] // Change to meet your customizability requirements
    public boolean isRetryable() // Use final if you want to prevent overriding
    {
        return false; // You can also use true if you want to enforce retryable behavior
    }
    ...
} 

//SysOperationServiceController 
class TestBatchJob extends SysOperationServiceController implements BatchRetryable
{
    [Wrappable(true), Replaceable(true)] // Change to meet your customizability requirements
    public boolean isRetryable() // Use final if you want to prevent overriding
    {
        return false; // You can also use true if you want to enforce retryable behavior
    }
    ...
}
```

### <a name="i-am-extending-a-microsoft-batch-that-is-retryable-but-my-batch-job-isnt-retryable-will-the-retry-be-triggered"></a>再試行可能な Microsoft バッチを拡張していますが、バッチ ジョブを再試行できません。 再試行をトリガーしますか?

追加ジョブで **isRetryable** が **false** に設定されている場合、ジョブは再試行されません。

### <a name="i-mistakenly-marked-my-custom-job-as-retryable-can-i-override-without-taking-another-code-change"></a>間違ってカスタム ジョブを再試行可能とマークしました。 コード変更せずに上書きできますか?

はい。 コードを変更しなくても SQL サーバーの接続損失が起きた場合、**システム管理 \> 設定 \> バッチ クラス コンフィギュレーションの上書き** をクリックし、再試行からクラスの接続を解除します。 **バッチ クラス コンフィギュレーションの上書き** ページで、新しいレコードを作成し、接続を解除するバッチ クラスを追加する必要があります。 この機能を使用して、必要な変更に迅速に対応できます。 ベスト プラクティスの推奨事項は、コードの更新を確認することです。

### <a name="my-batch-jobs-are-designed-to-run-multithreaded-how-do-i-implement-retries"></a>自分のバッチ ジョブは、マルチスレッドを実行するように設計されています。 再試行を実行するにはどうしたらよいですか?

カスタム バッチ プロセスがマルチスレッドで実行するように設計されている場合 (つまり、複数のタスクを作成してランタイム タスクを追加する場合)、メイン コントローラーとタスク コントローラーの両方に **BatchRetryable** インターフェイスを実装する必要があります。

### <a name="what-is-the-best-practice-for-the-execution-time-for-a-batch-job"></a>バッチ ジョブの実行時間のベスト プラクティスは何ですか?

実行時間が短いバッチ ジョブの方が正常に完了する可能性が高くなります。 そのため、再試行の必要が回避されます。

### <a name="what-is-the-best-practice-for-the-transaction-size-for-a-batch-job"></a>バッチ ジョブのトランザクション サイズのベスト プラクティスは何ですか?

トランザクション サイズが小さいバッチ ジョブは、障害によって失われる可能性がある作業の量を減らします。 したがって、再試行の必要性によって、合計実行時間は大幅に長くなりません。

### <a name="what-does-idempotent-mean-for-a-batch-job"></a>バッチ ジョブのべき等とは何ですか?

このコンテキストでは、*べき等* とはつまり再試行によって結果全体が変更されたり、影響を受けないことです。 たとえば、あるものは 1 回だけ操作を実行する必要があり、1 回以上は実行しません。 そのため、元の実行で実行されたあるものは再試行の際に再度実行されません。

### <a name="can-i-change-the-maximum-number-of-retries-and-the-retry-interval"></a>再試行の最大回数と再試行間隔は変更できますか?

**BatchRetryable** インターフェイスにより、一時的な SQL 接続の問題を処理できるようになります。 主にフレームワークによって制御します。 再試行の最大回数や再試行間隔など、**BatchRetryable** の設定を顧客が更新することはできません。

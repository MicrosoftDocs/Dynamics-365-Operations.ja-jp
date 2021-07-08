---
title: バッチ ジョブで自動再試行を有効にする
description: このトピックでは、障害が発生した場合にバッチ ジョブで自動再試行を有効にする方法について説明します。
author: sarvanisathish
ms.date: 06/10/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2021-05-31
ms.openlocfilehash: 0ded7474dd5bf0b69763f2fd45109e9ee5c3395e
ms.sourcegitcommit: 257437a57e146496a49782bc8aad179c92fbf6e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2021
ms.locfileid: "6224990"
---
# <a name="enable-automatic-retries-on-batch-jobs"></a>バッチ ジョブで自動再試行を有効にする

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリのバッチ ジョブで再試行を実装する方法、および障害が発生した場合に自動再試行を有効にする方法について説明します。 現在、Finance and Operations アプリの Microsoft SQL Server への接続が簡単に失われると、すべてのバッチ ジョブが失敗します。 この動作により業務プロセスが中断します。 クラウド サービスでは接続が失われることは避けられないので、Microsoft はこのタイプのエラーが発生した場合の自動再試行を有効にしています。

## <a name="metadata"></a>メタデータ

すべてのバッチ ジョブがべき等でない可能性もある (バッチでクレジット カード トランザクションを実行する場合など) ため、すべてのバッチ ジョブで再試行を等しく有効にすることはできません。 再試行を安全に有効にできるよう、Microsoft はバッチ ジョブにメタデータを追加して、自動的に再試行できるかどうか表示するようにしました。 バージョン 10.0.18 と 10.0.19 の間では、Microsoft バッチ ジョブの 90% 以上が明示的に **BatchRetryable** インターフェイスを実装し、**isretryable** 値は適切に設定されました。 **BatchRetryable** インターフェイスを実装していないすべてのジョブで、**isRetryable** の既定値は **false** です。

## <a name="retries"></a>再試行

**BatchRetryable** インターフェイスが実装され、**isRetryable** が **true** に設定されているジョブに対してのみ再試行は有効になります。 この新しい機能では、SQL Server 接続が中断する場合に再試行が発生します。 Microsoft は引き続き、他の例外での再試行を追加します。

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

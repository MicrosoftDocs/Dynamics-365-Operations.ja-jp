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
# <a name="enable-automatic-retries-on-batch-jobs"></a><span data-ttu-id="9b498-103">バッチ ジョブで自動再試行を有効にする</span><span class="sxs-lookup"><span data-stu-id="9b498-103">Enable automatic retries on batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b498-104">このトピックでは、Finance and Operations アプリのバッチ ジョブで再試行を実装する方法、および障害が発生した場合に自動再試行を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b498-104">This topic describes how retries are implemented on batch jobs in Finance and Operations apps, and how you can enable automatic retries on batch jobs when transient failures occur.</span></span> <span data-ttu-id="9b498-105">現在、Finance and Operations アプリの Microsoft SQL Server への接続が簡単に失われると、すべてのバッチ ジョブが失敗します。</span><span class="sxs-lookup"><span data-stu-id="9b498-105">Currently, if Finance and Operations apps experience a brief loss of connection to Microsoft SQL Server, all batch jobs that are running fail.</span></span> <span data-ttu-id="9b498-106">この動作により業務プロセスが中断します。</span><span class="sxs-lookup"><span data-stu-id="9b498-106">This behavior disrupts business processes.</span></span> <span data-ttu-id="9b498-107">クラウド サービスでは接続が失われることは避けられないので、Microsoft はこのタイプのエラーが発生した場合の自動再試行を有効にしています。</span><span class="sxs-lookup"><span data-stu-id="9b498-107">Because connection loss is inevitable in a cloud service, Microsoft is enabling automated retries when failures of this type occur.</span></span>

## <a name="metadata"></a><span data-ttu-id="9b498-108">メタデータ</span><span class="sxs-lookup"><span data-stu-id="9b498-108">Metadata</span></span>

<span data-ttu-id="9b498-109">すべてのバッチ ジョブがべき等でない可能性もある (バッチでクレジット カード トランザクションを実行する場合など) ため、すべてのバッチ ジョブで再試行を等しく有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9b498-109">Because not all batch jobs might be idempotent (for example, when a batch runs credit card transactions), retries can't be enabled equally across all batch jobs.</span></span> <span data-ttu-id="9b498-110">再試行を安全に有効にできるよう、Microsoft はバッチ ジョブにメタデータを追加して、自動的に再試行できるかどうか表示するようにしました。</span><span class="sxs-lookup"><span data-stu-id="9b498-110">To help ensure that retries can safely be enabled, Microsoft has added metadata to the batch jobs to indicate whether they can automatically be retried.</span></span> <span data-ttu-id="9b498-111">バージョン 10.0.18 と 10.0.19 の間では、Microsoft バッチ ジョブの 90% 以上が明示的に **BatchRetryable** インターフェイスを実装し、**isretryable** 値は適切に設定されました。</span><span class="sxs-lookup"><span data-stu-id="9b498-111">Between versions 10.0.18 and 10.0.19, more than 90 percent of the Microsoft batch jobs have explicitly implemented the **BatchRetryable** interface, and the **isRetryable** value has been set appropriately.</span></span> <span data-ttu-id="9b498-112">**BatchRetryable** インターフェイスを実装していないすべてのジョブで、**isRetryable** の既定値は **false** です。</span><span class="sxs-lookup"><span data-stu-id="9b498-112">For any jobs where the **BatchRetryable** interface isn't implemented, the default value of **isRetryable** is **false**.</span></span>

## <a name="retries"></a><span data-ttu-id="9b498-113">再試行</span><span class="sxs-lookup"><span data-stu-id="9b498-113">Retries</span></span>

<span data-ttu-id="9b498-114">**BatchRetryable** インターフェイスが実装され、**isRetryable** が **true** に設定されているジョブに対してのみ再試行は有効になります。</span><span class="sxs-lookup"><span data-stu-id="9b498-114">Retries are enabled only for jobs where the **BatchRetryable** interface is implemented and **isRetryable** is set to **true**.</span></span> <span data-ttu-id="9b498-115">この新しい機能では、SQL Server 接続が中断する場合に再試行が発生します。</span><span class="sxs-lookup"><span data-stu-id="9b498-115">In this new functionality, retries occur on any interruption of the SQL Server connection.</span></span> <span data-ttu-id="9b498-116">Microsoft は引き続き、他の例外での再試行を追加します。</span><span class="sxs-lookup"><span data-stu-id="9b498-116">Microsoft will continue to add retries on other exceptions.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="9b498-117">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="9b498-117">Frequently asked questions</span></span>

### <a name="how-do-retries-work-for-my-custom-batch-jobs"></a><span data-ttu-id="9b498-118">自分のカスタム バッチ ジョブの再試行を実行するにはどうしたらよいですか?</span><span class="sxs-lookup"><span data-stu-id="9b498-118">How do retries work for my custom batch jobs?</span></span>

<span data-ttu-id="9b498-119">カスタム バッチ ジョブに変更はありません。</span><span class="sxs-lookup"><span data-stu-id="9b498-119">There is no change to the custom batch jobs.</span></span> <span data-ttu-id="9b498-120">自動再試行を活用するには、カスタム バッチ ジョブで **BatchRetryable** インターフェイスを明示的に実装し、**isRetryable** を **true** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9b498-120">To take advantage of automated retries, explicitly implement the **BatchRetryable** interface on the custom batch jobs, and set **isRetryable** to **true**.</span></span> <span data-ttu-id="9b498-121">安全に再試行できるようにバッチ ジョブを変更しなければならない場合があることに注意します。</span><span class="sxs-lookup"><span data-stu-id="9b498-121">Note that you might have to modify the batch jobs to ensure that they are safe to retry.</span></span>

### <a name="how-do-i-implement-the-retryable-interface"></a><span data-ttu-id="9b498-122">再試行可能なインターフェイスをどのようにして実装しますか?</span><span class="sxs-lookup"><span data-stu-id="9b498-122">How do I implement the retryable interface?</span></span>

<span data-ttu-id="9b498-123">バッチ クラスに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="9b498-123">Add the following code to your batch class.</span></span>

<span data-ttu-id="9b498-124">詳細については、[最終的な方法および Wrappable 属性](../extensibility/method-wrapping-coc.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b498-124">For more information, see [Final methods and the Wrappable attribute](../extensibility/method-wrapping-coc.md).</span></span>

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

### <a name="i-am-extending-a-microsoft-batch-that-is-retryable-but-my-batch-job-isnt-retryable-will-the-retry-be-triggered"></a><span data-ttu-id="9b498-125">再試行可能な Microsoft バッチを拡張していますが、バッチ ジョブを再試行できません。</span><span class="sxs-lookup"><span data-stu-id="9b498-125">I am extending a Microsoft batch that is retryable, but my batch job isn't retryable.</span></span> <span data-ttu-id="9b498-126">再試行をトリガーしますか?</span><span class="sxs-lookup"><span data-stu-id="9b498-126">Will the retry be triggered?</span></span>

<span data-ttu-id="9b498-127">追加ジョブで **isRetryable** が **false** に設定されている場合、ジョブは再試行されません。</span><span class="sxs-lookup"><span data-stu-id="9b498-127">Provided that **isRetryable** is set to **false** for the extended job, the job won't be retried.</span></span>

### <a name="i-mistakenly-marked-my-custom-job-as-retryable-can-i-override-without-taking-another-code-change"></a><span data-ttu-id="9b498-128">間違ってカスタム ジョブを再試行可能とマークしました。</span><span class="sxs-lookup"><span data-stu-id="9b498-128">I mistakenly marked my custom job as retryable.</span></span> <span data-ttu-id="9b498-129">コード変更せずに上書きできますか?</span><span class="sxs-lookup"><span data-stu-id="9b498-129">Can I override without taking another code change?</span></span>

<span data-ttu-id="9b498-130">はい。</span><span class="sxs-lookup"><span data-stu-id="9b498-130">Yes.</span></span> <span data-ttu-id="9b498-131">コードを変更しなくても SQL サーバーの接続損失が起きた場合、**システム管理 \> 設定 \> バッチ クラス コンフィギュレーションの上書き** をクリックし、再試行からクラスの接続を解除します。</span><span class="sxs-lookup"><span data-stu-id="9b498-131">You can go to **System administration \> Setup \> Batch class configuration overrides** to unregister your class from being retried when SQL Server connection failures occur, without having to go through a code change.</span></span> <span data-ttu-id="9b498-132">**バッチ クラス コンフィギュレーションの上書き** ページで、新しいレコードを作成し、接続を解除するバッチ クラスを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b498-132">On the **Batch class configuration overrides** page, you must create a new record and add the batch class that you want to unregister.</span></span> <span data-ttu-id="9b498-133">この機能を使用して、必要な変更に迅速に対応できます。</span><span class="sxs-lookup"><span data-stu-id="9b498-133">You can use this feature to react quickly to changes that are required.</span></span> <span data-ttu-id="9b498-134">ベスト プラクティスの推奨事項は、コードの更新を確認することです。</span><span class="sxs-lookup"><span data-stu-id="9b498-134">The best practice recommendation is to make sure that the code is updated.</span></span>

### <a name="my-batch-jobs-are-designed-to-run-multithreaded-how-do-i-implement-retries"></a><span data-ttu-id="9b498-135">自分のバッチ ジョブは、マルチスレッドを実行するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="9b498-135">My batch jobs are designed to run multithreaded.</span></span> <span data-ttu-id="9b498-136">再試行を実行するにはどうしたらよいですか?</span><span class="sxs-lookup"><span data-stu-id="9b498-136">How do I implement retries?</span></span>

<span data-ttu-id="9b498-137">カスタム バッチ プロセスがマルチスレッドで実行するように設計されている場合 (つまり、複数のタスクを作成してランタイム タスクを追加する場合)、メイン コントローラーとタスク コントローラーの両方に **BatchRetryable** インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b498-137">If your custom batch process is designed to run in multithreading (that is, if you're creating multiple tasks and adding runtime tasks), you must implement the **BatchRetryable** interface in both the main controller and the task controller.</span></span>

### <a name="what-is-the-best-practice-for-the-execution-time-for-a-batch-job"></a><span data-ttu-id="9b498-138">バッチ ジョブの実行時間のベスト プラクティスは何ですか?</span><span class="sxs-lookup"><span data-stu-id="9b498-138">What is the best practice for the execution time for a batch job?</span></span>

<span data-ttu-id="9b498-139">実行時間が短いバッチ ジョブの方が正常に完了する可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="9b498-139">A batch job that has a shorter execution time is more likely to be successfully completed.</span></span> <span data-ttu-id="9b498-140">そのため、再試行の必要が回避されます。</span><span class="sxs-lookup"><span data-stu-id="9b498-140">Therefore, the need for a retry is avoided.</span></span>
 
### <a name="what-is-the-best-practice-for-the-transaction-size-for-a-batch-job"></a><span data-ttu-id="9b498-141">バッチ ジョブのトランザクション サイズのベスト プラクティスは何ですか?</span><span class="sxs-lookup"><span data-stu-id="9b498-141">What is the best practice for the transaction size for a batch job?</span></span>

<span data-ttu-id="9b498-142">トランザクション サイズが小さいバッチ ジョブは、障害によって失われる可能性がある作業の量を減らします。</span><span class="sxs-lookup"><span data-stu-id="9b498-142">A batch job that has a smaller transaction size reduces the amount of work that can be lost because of a transient failure.</span></span> <span data-ttu-id="9b498-143">したがって、再試行の必要性によって、合計実行時間は大幅に長くなりません。</span><span class="sxs-lookup"><span data-stu-id="9b498-143">Therefore, the need for a retry won't drastically increase the total execution time.</span></span>

### <a name="what-does-idempotent-mean-for-a-batch-job"></a><span data-ttu-id="9b498-144">バッチ ジョブのべき等とは何ですか?</span><span class="sxs-lookup"><span data-stu-id="9b498-144">What does idempotent mean for a batch job?</span></span>

<span data-ttu-id="9b498-145">このコンテキストでは、*べき等* とはつまり再試行によって結果全体が変更されたり、影響を受けないことです。</span><span class="sxs-lookup"><span data-stu-id="9b498-145">In this context, *idempotent* means that a retry won't change or affect the overall result.</span></span> <span data-ttu-id="9b498-146">たとえば、あるものは 1 回だけ操作を実行する必要があり、1 回以上は実行しません。</span><span class="sxs-lookup"><span data-stu-id="9b498-146">For example, something should be done only one time and won't be done more than one time.</span></span> <span data-ttu-id="9b498-147">そのため、元の実行で実行されたあるものは再試行の際に再度実行されません。</span><span class="sxs-lookup"><span data-stu-id="9b498-147">Therefore, something that is done in the original run won't be done again during the retry.</span></span>

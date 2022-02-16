---
title: ライブ同期に関する二重書き込みの制限
description: このトピックでは、二重書き込みを使用して財務と運用アプリと Microsoft Dataverse にデータを書き込む際の制限について説明します。
author: nhelgren
ms.date: 08/31/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: nhelgren
ms.search.validFrom: 2021-08-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1a4b79b93daf21151748bf2e04f1ab3490f3c0e
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063634"
---
# <a name="dual-write-limits-for-live-synchronization"></a>ライブ同期に関する二重書き込みの制限

[!include [banner](../../includes/banner.md)]



より一貫した可用性とパフォーマンスのために、二重書き込みを使用して財務と運用アプリと Microsoft Dataverse にデータを書き込む際に制限が適用されます。 これらの制限は、二重書き込みのトランザクションをコントロールし、プラットフォーム レベルで適用されます。 シームレスな書き込みを確認し、エラーを最小限にするように設計されています。

財務と運用アプリおよび Dataverse には、多数のレコードと複雑な複数テーブルのトランザクションにまたがる多くのプロセスが含まれています。 各環境には、トランザクションの数、トランザクションごとのレコード数、およびトランザクション時間 (つまり、トランザクションの処理に必要な時間) に制限があります。 これらの制限および二重書き込みの Live 同期機能に対する影響を理解することは重要です。

## <a name="legal-entities"></a>法人
ライブ同期では、トランザクションごとに最大 250 の法人をサポートします。 これは、大きなデータ量および関連する操作によって 40 の法人のみがサポートされる初期同期とは異なります。

## <a name="transaction-patterns"></a>トランザクションのパターン

1 つのプロセスで、2 つの異なるトランザクション パターンでデータを書き込むことができます。

- **[1 つのトランザクション](#single-transaction)** – プロセスの一部として書き込まれるデータすべては、1 つのトランザクションの一部です。
- **[複数のトランザクション](#multiple-transactions)** – プロセスの一部として書き込まれるデータはすべて複数のトランザクションに分割されます。

### <a name="single-transaction"></a>1 つのトランザクション

1 つのトランザクションにおいて、プロセスの一部として書き込まれるデータすべては、1 つのトランザクションの一部です。 エラーが発生した場合、トランザクション全体がロールバックされます。

一般的な例として、1 つのトランザクションで複数の請求書を作成するプロセスがあります。 この場合、すべての請求書が 1 つのトランザクションで確定済みになるか、エラーが発生した場合にすべての請求書がロールバックされるかのいずれかです。 次のコード例では、1 つのトランザクションで複数の請求書を作成します。

```xpp
ttsbegin;// Transaction start
    Invoice1.create();
    Invoice2.create();
    Invoice3.create();
    // Additional invoices.
    InvoiceN.create();
ttscommit;// Transaction end
```

```xpp
ttsbegin;// Transaction start
    while (/* loop condition */)
    {
      InvoiceN.create();
    }
ttscommit;// Transaction end
```

### <a name="multiple-transactions"></a>複数のトランザクション

複数のトランザクションにおいて、プロセスの一部として書き込まれるデータはすべて複数のトランザクションに分割されます。 エラーが発生した場合、複数のトランザクションのグループ全体はロールバックされません。 代わりに、各トランザクションは個別にロールバックされるかまたは確定されます。 失敗したトランザクションはすべてロールバックされます。 失敗しなかったトランザクションはすべて確定されます。

一般的な例として、複数の請求書を作成するプロセスがあります。 各請求書は個別のトランザクションで作成され、エラーが発生した場合は、特定のトランザクションに含まれている請求書だけがロールバックされます。 残りの請求書は正常に確定されます。 次のコード例では、トランザクションごとに 1 つずつ、複数の請求書を作成します。

```xpp
ttsbegin; // Transaction start
    Invoice1.create();
ttscommit;// Transaction end

ttsbegin;// Transaction start
    Invoice2.create();
ttscommit;// Transaction end

ttsbegin;// Transaction start
    Invoice3.create();
ttscommit;// Transaction end

// Additional transactions.

ttsbegin;// Transaction start
    InvoiceN.create();
ttscommit;// Transaction end
```

```xpp
while (/* loop condition */)
{
    ttsbegin;// Transaction start
    InvoiceN.create();
    ttscommit;// Transaction end
}
```

## <a name="transaction-time-limit"></a>トランザクションの制限時間

二重書き込みを使用して財務と運用アプリまたは Dataverse にレコードを書き込む場合、各トランザクションは特定の時間内に完了する必要があります。 トランザクションの制限時間に達する前にトランザクションが完了しない場合、二重書き込みを使用して財務と運用アプリと Dataverse にレコードが確定されることはありません。 この場合、トランザクション内のレコードは、Finance and Operations 環境と Dataverse 環境の両方でロールバックされます。

たとえば、二重書き込みを使用して財務と運用アプリから Dataverse に契約の更新を同期する場合、財務と運用アプリのビジネス ロジックが完了し、Dataverse プロセスが開始される時にタイマーが開始されます。 トランザクションが確定される時にタイマーは終了します。 Dataverse で費やされた時間全体には、書き込み必要な時間、標準およびカスタムのプラグインを処理するのに必要な時間も含まれます。 トランザクションが制限時間を超えた場合、Dataverse にレコードは確定されません。

二重書き込みを使用して Dataverse から財務と運用アプリに逆の方向でデータを書き込む場合にも同じ原則が適用されます。

## <a name="dual-write-live-synchronization-limits"></a>二重書き込みのライブ同期の制限

次の表は、財務と運用アプリと Dataverse 間でデータを書き込む時に適用される二重書き込みのライブ同期の制限を示しています。 これらの制限はデータ フローの方向に対して固有です: 財務と運用アプリから Dataverse へ、または Dataverse から財務と運用アプリへ。

### <a name="from-finance-and-operations-apps-to-dataverse"></a>財務と運用アプリから Dataverse へ

財務と運用アプリから Dataverse にデータを書き込む場合、次の制限が適用されます。

| 措置 | 制限 |
|---|---|
| トランザクションの数 | テナントごとに 1 日あたり実行できるトランザクションの合計数は、クライアント アプリケーションがサーバー リソースに対して特別な要求を行う場合に検出するように設計されたサービス保護 API の制限によって管理されます。 詳細については、[サービス保護 API の制限](/powerapps/developer/data-platform/api-limits)を参照してください。 |
| 1 つのトランザクションあたりのレコード数 | <p>1,000 レコード</p><p>1 つのトランザクションのレコードが 1,000 件を超える場合、そのトランザクションを複数のトランザクションに分割することを検討してください。 詳細については、このトピックの [1,000 レコードを超えるトランザクション ](#transactions-with-more-than-1000-records)を参照してください。</p> |
| トランザクションの制限時間 | 2 分 |

### <a name="from-dataverse-to-finance-and-operations-apps"></a>Dataverse から財務と運用アプリへ

Dataverse から財務と運用アプリにデータを書き込む場合、次の制限が適用されます。

| 措置 | 制限 |
|---|---|
| トランザクションの数 | トランザクションの数は、リソースの過剰使用率を回避してシステムの応答性を維持するために設計された優先順位に基づく調整の制限の影響を受けることがあります。 詳細については、[優先順位に基づく調整](../priority-based-throttling.md)を参照してください。 |
| 1 つのトランザクションあたりのレコード数 | <p>Dataverse のペイロード サイズの制限により、転送可能なレコードの数は制限されます。 トランザクションごとの制限は 116.85 メガバイト (MB) です。 詳細については、[エラー: コンテキストをサンドボックスに送信するときにメッセージ サイズが超過しました](/powerapps/developer/data-platform/troubleshoot-plug-in#error-message-size-exceeded-when-sending-context-to-sandbox)を参照してください。 この制限の使用は、エンティティの複雑さ、使用される列の種類、およびマップされたフィールドなどの複数の要素によって異なります。 したがって、制限を単純なレコード数として表すことはできません。</p><p>制限を超過した場合、Dataverse はトランザクション (*メッセージ* と呼ばれる) を拒否し、次のエラー コードが使用されます。</p><p>*エラー コード: -2147220970 エラー メッセージ: コンテキストをサンドボックスに送信するときにメッセージ サイズが超過しました。メッセージ サイズ: ### MB*</p><p>1 つのトランザクションのレコード サイズが 116.65 MB を超える場合、トランザクションを複数のトランザクションに分割することを検討してください。 詳細については、このトピックの [1,000 レコードを超えるトランザクション ](#transactions-with-more-than-1000-records)を参照してください。</p> |
| トランザクションのタイムアウト | 2 分 |

## <a name="transactions-with-more-than-1000-records"></a>1,000 レコードを超えるトランザクション

トランザクションのレコードが 1,000 件を超えるシナリオは、一般的です。 これらのシナリオにおいて、1 つのトランザクションを複数のトランザクションに分割することをお勧めします。 次のコード例で、レコード ID に基づいて複数のトランザクションを作成する方法を示します。

```xpp
ttsbegin;// Transaction start.
    Invoice1.create();
    Invoice2.create();
    // Additional invoices.
    Invoice1000.create();
ttscommit;// Transaction end.

ttsbegin;// Transaction start.
    Invoice1001.create();
    Invoice1002.create();
    // Additional invoices.
    Invoice2000.create();
ttscommit;// Transaction end.

ttsbegin;// Transaction start.
    Invoice2001.create();
    Invoice2002.create();
    // Additional invoices.
    Invoice3000.create();
ttscommit;// Transaction end.

// Additional transactions.

ttsbegin;// Transaction start.
    Invoice(N)1.create();
    Invoice(N)2.create();
    // Additional invoices.
    Invoice(N+1)000.create();
ttscommit;// Transaction end.
```

```xpp
i = 1;
committPending = false;
while (/* loop condition */)
{
    if (i==1) 
    {
        ttsbegin;// Transaction start.
        committPending = true;
    }
    InvoiceN.create();
    if (i == 1000)
    {
        ttscommit;// Transaction end.
        committPending = false;
        i = 0;
    }

    i++;
}

if (committPending == true)
{
    ttscommit; // Transaction end.
}
```

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

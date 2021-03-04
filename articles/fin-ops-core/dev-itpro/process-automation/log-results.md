---
title: 結果とメッセージを記録する
description: このトピックでは、プロセスの自動化から結果およびメッセージを記録する方法について説明します。
author: RyanCCarlson2
manager: AnnBe
ms.date: 09/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-09-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc5aae5a4724380928def8bdc11460db06521a02
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680410"
---
# <a name="log-results-and-messages"></a>結果とメッセージを記録する

[!include [banner](../includes/banner.md)]

プロセス自動化フレームワークでは、結果およびメッセージのログ記録がサポートされています。 プロセスが結果とメッセージを記録するには、次の 2 つの理由があります。

- 結果とメッセージ ログは、プロセスの状態をシステム管理者またはアクセス権を持つその他のロールに伝達します。 プロセスの結果を監視して、他のユーザーに表示することが重要です。 障害が発生した場合は、修復するか、プロセスの所有者との間で問題を提起することができます。
- 結果は、プロセスで行われた内容を伝達する必要があります。 たとえば、プロセスが仕入先請求書を転記する場合、結果にはすべての仕入先請求書が表示されます。 この場合、各結果には、仕入先請求書へのステータスとリンクが表示されます。

結果およびメッセージは、複数レベルのログ システムです。 プロセスには 1 つ以上の結果があります。 各結果には、それに固有のメッセージが 1 つ以上含まれます。 メッセージは、結果の合成子です。 結果は通常、プロセスが処理しているものです。 たとえば、プロセスが仕入先請求書を転記する場合、結果として各仕入先請求書をログに記録します。 その後、各仕入先請求書を転記するたびに、その結果に関連付けられている複数のメッセージをログに記録できます。 仕入先請求書が正常に転記された場合、ユーザーが結果を参照すると操作の成功が明らかなので、メッセージ ログを空白のままにできます。 警告が発生した場合は、転記が成功した場合でも警告をメッセージ ログに書き込む必要があります。 これらのメッセージによって透明度が提供され、ユーザーは各プロセスの実行内容や結果を確認することができます。

スケジュールされたプロセスとポーリングされたプロセスは共に、結果とメッセージのログ記録をサポートします。 すべてのプロセスは、結果を作成する必要があります。 少なくとも、結果はすべて成功したという事実を伝える必要があります。 ユーザーの作業に影響を与え、ユーザーに表示される作業を行うプロセスは、より詳細な結果を作成する必要があります。 以前に使用された仕入先請求書の転記の例では、ユーザーは請求書が転記されていることを確認する必要がある場合があります。 情報が他の方法で使用可能な場合でも、情報が混乱する可能性がある結果は表示しません。

次の図は、結果ビューを示しています。

![結果の状態、時間、およびメッセージ](media/execution-results.png)

次の図は、メッセージ ビューを示しています。 このビューを開くには、結果ビューで **ログ** 列の **ログの表示** を選択します。

![個々のメッセージの例外タイプとメッセージ](media/execution-message-log.png)

## <a name="processexecutionsourcelink-table"></a>ProcessExecutionSourceLink テーブル

**ProcessExecutionSourceLink** テーブルには、処理の実行中に作成された結果が含まれます。 このテーブルには、**RefTableId** と **RefRecId** フィールドが含まれています。 これらのフィールドは、Microsoft SQL Server 内の任意のソース レコードにリンクされており、通常はプロセスが処理しているものです。 このテーブルには、**ヘッダー** および **メッセージ** フィールドも含まれます。 **ヘッダー** フィールドは、結果グリッドの列として表示されます。 メッセージは任意のものにすることができます。

たとえば、仕入先支払提案が支払仕訳帳を作成している場合、**RefTableId** 値は **LedgerJournalTable** テーブルのテーブル ID です。 **RefRecId** 値は、実行中のプロセスによって作成された支払仕訳帳の **LedgerJournalTable** レコードの **RecId** 値です。 この場合、**ヘッダー** フィールドを仕訳帳番号に設定できます。 この値をジャンプ参照に設定して、ユーザーが支払仕訳帳に直接移動するための仕訳帳番号を選択できるようにすることもできます。 **支払仕訳帳が正常に作成された** など、表示したい任意のメッセージに **メッセージ** フィールドを設定できます。

多数の品目を処理するプロセス (たとえば、多数の請求書を転記している場合など) では、各請求書に対して **ProcessExecutionSourceLink** レコードを作成できます。

プロセスが処理している品目の数が非常に多く (数百万単位)、また、ユーザーが各品目の詳細を確認する必要がない場合は、それらの品目をバッチに要約することを検討してください。 たとえば、一般会計に対する補助元帳の転送のプロセスでは、転送された各伝票に対してではなく、一般会計に転送された各転送 ID に対して **ProcessExecutionSourceLink** レコードが作成されます。

| メソッド | 説明 |
|---|---|
| `public static void insertSourceLinks(ProcessScheduleTypeName _typeName, ProcessExecutionSourceLinkTmp _tmp)` | このメソッドはバージョン 10.0.14 の新機能です。 セットベースの挿入を使用して、**ProcessExecutionSourceLink** テーブルに多数の結果を挿入します。 |
| `public static ProcessExecutionSourceLink insertSourceLink(ProcessExecutionSourceLinkItem _sourceLinkItem)` | このメソッドは、**ProcessExecutionSourceLink** テーブルにレコードを挿入します。 |

## <a name="processexecutionsourcelinkitem-class"></a>ProcessExecutionSourceLinkItem クラス

**ProcessExecutionSourceLinkItem** クラスをインスタンス化し、ソース品目を正しく表示するために必要な値を入力します。

| メソッド | 説明 |
|---|---|
| `public static ProcessExecutionSourceLinkItem newFromProcessScheduleWorkItemAndStatus(ProcessScheduleWorkItem _workItem, ProcessExecutionSourceStatus _status)` | このコンストラクターを使用して、**ProcessExecutionSourceLinkItemの** インスタンスを作成します。 このメソッドは、**processscheduleworkitem** から必要なフィールドの多くを正しく初期化します。 |
| `public static ProcessExecutionSourceLinkItem newFromProcessExecutionSourceLink(RefRecId _processExecutionSourceLinkRecId)` | このメソッドは、**ProcessExecutionSourceLinkItem** のインスタンスを構築し、**ProcessExecutionSourceLink** レコードの指定されたレコード ID を使用してインスタンスを初期化し ます。 |
| `public RefRecId parmSourceRecId(RefRecId _sourceRecId = sourceRecId)` | ソース レコードのレコード ID を設定します。 たとえば、この値は、仕入先請求書ヘッダー テーブルのレコード ID である場合があります。 |
| `public RefTableId parmSourceTableId(RefTableId _sourceTableId = sourceTableId)` | ソース テーブルのテーブル ID を設定します。 たとえば、この値は、仕入先請求書ヘッダー テーブルのテーブル ID である場合があります。 |
| `public ProcessExecutionSourceLinkHeader parmHeader(ProcessExecutionSourceLinkHeader _header = header)` | ヘッダー フィールドの値を設定します。 以前に使用された仕入先請求書の転記の例では、この値は請求書番号である場合があります。 |
| `public ProcessExecutionSourceLinkMessage parmMessage(ProcessExecutionSourceLinkMessage _message = message)` | メッセージを設定します。 以前に使用された仕入先請求書の転記の例では、この値は **転記成功** である場合があります。 |
| `public ProcessExecutionId parmExecutionId(ProcessExecutionId _executionId = executionId)` | このメソッドは、実行 ID を設定します。 この値は、**ProcessAutomationTask** インターフェイスの実装で **processscheduleworkitem** を介して提供されています。 |

## <a name="processexecutionmessagelog-table"></a>ProcessExecutionMessageLog テーブル

**ProcessExecutionMessageLog** テーブルには、単一の **ProcessExecutionSourceLink** レコードに関連するメッセージが含まれています。 このテーブルには、任意のタイプのメッセージを書き込むことができます。 その後、メッセージがユーザーに表示されます。

| メソッド | 説明 |
|---|---|
| `public static void insertMessages(ProcessScheduleTypeName _typeName, ProcessExecutionMessageLogTmp _tmp)` | このメソッドでは、セット ベースの挿入を使用して、**ProcessExecutionMessageLog** テーブルにメッセージを挿入します。 |
| `public static ProcessExecutionMessageLog insertMessage(ProcessExecutionMessageLogItem _errorLogItem)` | このメソッドは、メッセージをメッセージログに挿入します。 |

## <a name="processexecutionmessagelogitem-class"></a>ProcessExecutionMessageLogItem クラス

メッセージ ログには、メッセージが文字列とラベル ID の両方ろして格納されます。 両方の値を設定する必要はありません。 ラベル ID は、メッセージ ログのユーザー インターフェイス (UI) 内のメッセージの変換をサポートしているので、推奨されます。 ただし、メッセージは、ラベル ID のログをサポートしないプロセスとの下位互換性のために提供されています。

シナリオに応じて適切なコンストラクターを使用します。

| メソッド | 説明 |
|---|---|
| `public static ProcessExecutionMessageLogItem newFromProcessExecutionSourceLinkAndMessage(RefRecId _processExecutionSourceLinkRecId, Exception _exception, ProcessExecutionMessage _message)` | |
| `public static ProcessExecutionMessageLogItem newFromProcessExecutionSourceLinkAndLabel(RefRecId _processExecutionSourceLinkRecId, Exception _exception, LabelId _labelId, container _labelParameters)` | |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
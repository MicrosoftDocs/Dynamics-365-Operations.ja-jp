---
title: 財務諸表に関するよく寄せられる質問
description: この記事では、よく寄せられる財務諸表に関するいくつかの質問に対する回答を提供します。
author: jinniew
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5981946a4bba2c58402f4cf566bfa008de67363b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901373"
---
# <a name="financial-reporting-faq"></a>財務諸表に関するよく寄せられる質問

この記事では、よく寄せられる財務諸表に関する質問に対する回答を提供します。

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>ツリー セキュリティを使用して、レポートへのアクセスを制限するにはどうすればよいですか。

次の例は、ツリー セキュリティを使用してレポートへのアクセスを制限する方法を示しています。

USMF デモ会社には、財務諸表のすべてのユーザーがアクセスすべきではない **貸借対照表** レポートがあります。 ツリー セキュリティを使用すると、あるレポートへのアクセスを制限して、特定のユーザーのみがそれにアクセスできるようにすることができます。

1. Financial Reporter Report Designer にサインインします。
2. **ファイル \> 新規 \> ツリー定義** の順に選択して新しいツリー定義を作成します。
3. **ユニットのセキュリティ** 列の **集計** 行をダブルタップ (またはダブルクリック) します。
4. **ユーザーとグループ** を選択します。
5. レポートにアクセスする必要があるユーザーまたはグループを選択します。
6. **保存** を選択します。
7. レポート定義で、新しいツリー定義を追加します。
8. ツリー定義で、**設定** を選択します。 **レポート ユニットの選択** で、**すべてのユニットを含む** を選択します。

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>残高と一致しない勘定は、どのように識別できますか。

残高が一致しないレポートがある場合は、以下の手順に従って、各勘定と差異を特定します。

### <a name="in-financial-reporter-report-designer"></a>Financial Reporter Report Designer 内

1. 新しい行定義を作成します。
2. **編集 \> 分析コードからの行の挿入** を選択します。
3. **MainAccount** を選択します。
4. **OK** を選択します。
5. 行定義を保存します。
6. 新しい列定義を作成します。
7. 新しいレポート定義を作成します。
8. **設定** を選択し、このオプションのマークを解除します。
9. レポートを生成します。 
10. レポートを Microsoft Excel にエクスポートします。

### <a name="in-dynamics-365-finance"></a>Dynamics 365 Finance 内

1. **一般会計 \> 照会およびレポート \> 試算表** の順に進みます。
2. 次のフィールドを設定します。

    - **開始日** – 会計年度の開始日を入力します。
    - **終了日** – レポートを生成する日を入力します。
    - **財務分析コード** – このフィールドを **主勘定セット** に設定します。

3. **計算** を選択します。
4. レポートを Excel にエクスポートします。

これで、Financial Reporter Excel レポートから **試算表** レポートにデータをコピーして、**決算残高** 列を比較できます。

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Report Designer でレポートを設計したり、財務諸表を生成する場合に、「データ プロバイダー フレームワークの問題が原因で操作を完了できません」というメッセージが表示されます。 対応方法を教えてください。

このメッセージは、財務諸表の使用中にシステムがデータ マートから財務メタデータを取得しようとしたときに問題が発生したことを示します。 この問題に対応するには、次の 2 つの方法があります。

- Report Designer の **ツール \> 統合の状態** に移動して、データの統合の状態を確認します。 統合が不完全な場合は、完了するまで待ちます。 その後、メッセージを受信したときに行っていた操作を再試行します。
- サポートに問い合わせ、問題を特定して作業してください。 システムにデータの不整合がある可能性があります。 サポート エンジニアは、サーバー上の問題を特定し、更新が必要な可能性がある特定のデータを探す支援を行うことができます。

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>履歴レート換算を選択するとレポートのパフォーマンスにどのような影響を及ぼしますか?

履歴レートは一般に、利益剰余金、資産、プラントや設備、および株主資本の勘定で使用されます。 履歴レートは、財務会計基準委員会 (FASB) または一般に認められている会計原則 (GAAP) のガイドラインに基づいて、必要になる場合があります。 詳細については、[財務諸表の通貨の機能](financial-reporting-currency-capability.md)を参照してください。

## <a name="how-many-types-of-currency-rate-are-there"></a>通貨レートにはいくつのタイプがありますか?

次の 3 つのタイプがあります:

- **現在のレート** – このタイプは通常、貸借対照表勘定で使用されます。 一般に *スポット為替レート* と呼ばれ、月の最終日または別のあらかじめ設定された日付のレートです。
- **平均レート** – このタイプは一般に、損益計算書 (損益) 勘定で使用されます。 平均レートは、単純平均または加重平均のいずれかを実行するために設定できます。
- **履歴レート** – このタイプは一般に、利益剰余金、資産、プラントや設備、および株主資本の勘定で使用されます。 これらの勘定は、FASB または GAAP のガイドラインに基づいて、必要になる場合があります。

## <a name="how-does-historical-currency-translation-work"></a>履歴通貨換算はどのように機能しますか?

レートはトランザクション日付に固有です。 そのため、各トランザクションは、最も近い為替レートに基づいて個別に換算されます。

履歴通貨換算では、個々のトランザクションの詳細ではなく、事前に計算された期間残高を使用できます。 この動作は、現在のレート換算の動作とは異なります。

## <a name="how-does-historical-currency-translation-affect-performance"></a>履歴通貨換算はパフォーマンスにどのような影響を及ぼしますか?

レポートに表示されるデータが更新された場合、トランザクションの詳細を確認して金額を再計算する必要が生じるため、遅延が生じ得る場合があります。 この遅延は、レートが更新されるか、さらにトランザクションが転記されるごとにトリガーされます。 たとえば、1 日に 2 回の履歴換算のために何千もの勘定が設定されている場合、レポートのデータが更新される前に最大 1 時間の遅延が発生する場合があります。 一方、特定の勘定の数が少ない場合、レポート データの更新にかかる処理時間を数分以下に短縮できます。

同様に、履歴タイプの勘定に対して為替換算を使用してレポートが生成される場合は、トランザクションごとの計算が追加されます。 勘定数によっては、レポート生成時間が 2 倍を超えることがあります。

## <a name="what-are-the-estimated-data-mart-integration-intervals"></a>データ マートの推定統合間隔はどれくらいですか?

Financial Reporter は、Dynamics 365 Finance から Financial Reporter データベースにデータをコピーする際に、16 件のタスクを使用します。 これら 16 件のタスクを次の表にまとめ、それぞれのタスクについて実行頻度を決定する間隔を示します。 この間隔は変更できません。

| 名前                                                       | 間隔 | 間隔のタイミング |
|------------------------------------------------------------|----------|-----------------|
| AX 2012 勘定カテゴリから勘定カテゴリへ            | 41       | 分         |
| AX 2012 勘定から勘定へ                                | 7        | 分         |
| AX 2012 会社から会社へ                               | 300      | 秒         |
| AX 2012 会社から組織へ                          | 23       | 分         |
| AX 2012 分析コードの組み合わせから、分析コードの組み合わせへ    | 1        | 分         |
| AX 2012 分析コード値から分析コード値へ                | 11       | 分         |
| AX 2012 分析コードから分析コードへ                            | 31       | 分         |
| AX 2012 為替レートから為替レートへ                    | 17       | 分         |
| AX 2012 会計年度から会計年度へ                        | 13       | 分         |
| AX 2012 一般会計トランザクションからファクトへ                | 1        | 分         |
| AX 2012 組織階層からツリーへ                   | 3,600    | 秒         |
| AX 2012 シナリオからシナリオへ                              | 29       | 分         |
| AX 2012 トランザクション タイプ修飾子から、ファクト タイプ修飾子へ | 19       | 分         |
| メンテナンス タスク                                           | 1        | 分         |
| MR レポート定義から AX7 財務諸表へ             | 45       | 秒         |
| MR レポート バージョンから AX 財務諸表バージョンへ         | 45       | 秒         |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

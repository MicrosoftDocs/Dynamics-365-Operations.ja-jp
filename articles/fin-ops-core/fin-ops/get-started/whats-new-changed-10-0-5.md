---
title: 財務と運用アプリ バージョン 10.0.5 (2019 年 10 月) の新機能および変更された機能
description: この記事では、財務と運用アプリ バージョン 10.0.5 の新機能または変更された機能について説明します。 このバージョンは 10 月にリリースされます。
author: sericks007
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: fb88c68fbcd1642fdde10bb8b56cec0b0da522c6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287098"
---
# <a name="whats-new-or-changed-in-finance-and-operations-apps-version-1005-october-2019"></a>財務と運用アプリ バージョン 10.0.5 (2019 年 10 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 Finance と Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.5 を含む財務と運用アプリの新機能または変更された機能について説明します。 このバージョンのビルド番号は 10.0.197 です。 一般提供開始日は 10 月ですが、新機能は 8 月の初期リリースで使用できます。 バージョン 10.0.5 の詳細については [追加リソース](whats-new-changed-10-0-5.md#additional-resources) を参照してください。


最新のリリースの Dynamics 365 Retail の新機能と変更については、[Dynamics 365 for Retail バージョン 10.0.5 の新機能と変更](../../../commerce/get-started/whats-new-10-0-5.md) を参照してください。


## <a name="revenue-recognition"></a>収益認識

収益認識基準は、米国内の一般的に認められている会計原則 (GAAP) および国際財務報告基準 (IFRS) 要件を満たすための、ハードウェア、ソフトウェア、サポート、およびサブスクリプションの収益価格と収益スケジュールを定義することができます。

- **収益価格** - リリースされた製品に対して収益価格を定義し、その後収益を認識する価格を決定するために使用できます。 収益価格は、顧客に提供される販売価格とは異なる場合があります。

- **収益スケジュール** - 収益スケジュールによって、収益遅延の月数が決まります。 その月の実際の日付に基づいて、月に均等に配分、または発生した回数に基づいてスケジュールを作成するオプションがあります。

- **複数の販売注文の再配賦** - 配賦を行うと、請求済の販売注文または新しい販売注文に新しい販売注文明細行が追加された後に、収益価格を再計算できます。 その他の品目が元の契約合意に含まれている必要がある場合は、新しい行が再配賦されます。

- **ワークスペース** - この新しいワークスペースは、繰延収益に対して作成された収益スケジュールレコードのステータスを確認するために使用されます。

## <a name="cancel-bank-reconciliation"></a>口座調整のキャンセル

ユーザーは、口座の調整を最新のものから始まる順序でキャンセルすることができます。 履歴が追跡され、調整が取り消された時期と担当者が表示されます。 これにより、ユーザーは、定期処理中に発生したエラーを修正するために仕訳帳を手動で調整する必要がなくなります。

## <a name="create-checks-with-a-blank-status-on-the-checks-page"></a>[小切手] ページで空白状態の小切手を作成する

**小切手** ページでは、新しい小切手番号の作成や小切手の削除など、小切手に関するメンテナンスタスクを実行できます。 この機能が有効になっている場合は、支払プロセス中に空白ステータスの小切手を作成することはできず、その結果小切手在庫が無駄になります。

## <a name="reset-workflow-status-for-vendor-invoices"></a>仕入先請求書のワークフロー状態をリセットする

ワークフローの履歴ページを使用して、ワークフロー状態をドラフトにリセットできます。 このページは、**仕入先請求書** または **共通 > 照会 > ワークフロー** へ移動することで開くことができます。 ワークフロー状態をドラフトにリセットするには、**取り消し** を選択します。 また、**仕入先請求書** または **保留中の仕入先請求書** ページの **取り消し** アクションを選択して、ワークフロー状態をドラフトにリセットすることもできます。 ワークフロー ステータスをドラフトにリセットした後、**仕入れ先請求書** ページで編集できるようになります。

## <a name="dual-currency-consolidation"></a>デュアル為替連結

この機能は、連結会社のトランザクション通貨として使用される通貨 (会計通貨またはレポート通貨) をコントロールするのに役立ちます。 また、通貨が同じである場合は、ソース会社の金額を連結会社に自動的にコピーすることもできます。

- **統合オンラインフォームの連結金額を選択するを追加する** - この機能が有効になっている場合、ユーザーは、連結会社のトランザクション通貨として使用されるソース会社からの会計通貨またはレポート用通貨を、トランザクション通貨として使用するかどうかを選択できます。

- **通貨が同じである場合は、元の会社から連結会社に金額を直接コピーします** - この機能が有効化されていると、ソース会社の会計通貨金額またはレポートの通貨金額は、いずれかの通貨が同じである場合は、連結会社の会計通貨金額かレポートの通貨金額へと直接コピーされます。 連結会社の会計およびレポートの通貨金額は、いずれの通貨も同じでない場合は、為替レートを使用して計算されます。

## <a name="gender-in-currency-declension-for-eastern-europe"></a>東ヨーロッパの通貨declensionの性別 

通貨の性別を定義できるようになりました。 **通貨** ページで **Declension** を選択します。 **性別** フィールドで、**Masculine**、**Feminine**、または **Neuter** を選択します。 このパラメーターは、キャッシュ注文で現地の言語でテキストで書き込まれた金額のdeclensionに影響を与える可能性があります。 たとえば、金額 1,01 ユーロが英語の文字で、キャッシュオーダー上に *One euro 01 cent* として記載されている場合、**Neuter** として **性別** を設定すると、この金額がチェコ語に翻訳され、、*Edno euro 01 cent* として記載されます。

既存の機能の詳細については、[「レポートおよびドキュメント上の金額の表示方法の更新」](../../../finance/localizations/emea-amount-printing-forms.md)を参照してください。

## <a name="cash-control-public-sector"></a>現金管理 (公的部門)

現金管理では、現金残高がない場合、またはトランザクションによって残高が定義された限度を下回る場合に、トランザクションが転記されないように制限 (しきい値) を定義できます。 買掛金勘定の仕入先請求書および一般勘定科目の詳細な元帳エントリは、作成、編集、および転記の際に検証されます。 トランザクションの転記によって、関連する現金口座の残高がその口座に定義された制限よりも少なくなる場合、ユーザーはエラーメッセージを受け取り、続行するためにはアカウントを変更する必要があります。

## <a name="forecast-position-distribution-public-sector"></a>予測ポジションの配布 (公的部門)

予測ポジションの財務分析コードの既定のテンプレートを管理するには、**予測ポジション** ページの **財務分析コード** のクイックタブにあるコントロールを使用します。 クイックタブの上部に表示されるグリッドには、すべての配分明細行の割合と共に表示されます。 クイックタブの下の部分には、予測ポジションの既定の分析コードが表示されます。

予測ポジションの既定の分析コードがあなたの組織の勘定科目表に対して適切であるかどうかを検証できます。 予測ポジションに対して、**予測ポジション** ページで、アクション ウインドウで **検証** を選択して、予測ポジションの財務分析コードの設定が有効かどうかを確認します。 この検証は簡単で、予測ポジションから予算計画を生成する前にエラーを識別するのに役立ちます。 **予測ポジション** ページでは、複数の予測ポジションを同時に検証することもできます。

## <a name="deferred-put"></a>繰延プット
繰延処理機能では、入力操作がバックグラウンドで処理されている間でも、倉庫作業者は他の作業を続行できます。 繰延処理では、多くの作業明細行を処理する必要があり、作業者がその作業を非同期に処理できるようにする場合に便利です。 また、サーバーが処理時間の増加をアドホックまたは計画外でおこない、増加した処理時間がユーザーの生産性に影響を与える可能性がある場合にも役立ちます。

詳細については、[倉庫作業の遅延処理](/dynamics365/unified-operations/supply-chain/warehousing/deferred-put)を参照してください。

## <a name="journal-unlock"></a>仕訳帳をロック解除する
仕訳帳ページの新しいボタンを使用して、**システムによってロック済み** のステータスに設定されている仕訳帳のロックを「はい」に設定することでロック解除することができます。 このロック解除は、実行しているバッチジョブを分析したシステム管理者が実行でき、この仕訳帳がバッチジョブによって積極的に処理されなくなったことを確認します。 このボタンは、**機能管理** ページにある **仕訳帳のロック解除** ボタンで有効にできます。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
バージョン 10.0.5 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=348248&dbType=3&qc=71f7c009fafc56f21399d05a7062454208256c806b7f5c706a89f4452964c26e) を参照してください。

### <a name="platform-update-29"></a>プラットフォーム update 29
バージョン 10.0.5 には、プラットフォーム更新プログラム 29 が含まれています。 プラットフォーム更新プロフラム 29 についての詳細は、[財務と運用アプリのプラットフォーム更新プログラム 29 の新機能や変更 (2019 年 10 月)](whats-new-platform-update-29.md) を参照してください。

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2019wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[財務と運用の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) の記事では、削除済みまたは非推奨の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に[財務と運用の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


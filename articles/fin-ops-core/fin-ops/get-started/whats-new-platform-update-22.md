---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 22 (2018 年 12 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operation プラットフォーム更新プログラム 22 (2018 年 12 月) の新機能または変更された機能について説明します。
author: tonyafehr
manager: AnnBe
ms.date: 02/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: b756a61c-52a3-47c5-b579-66b9249c592b
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Platform 22
ms.openlocfilehash: e0ed208be8eeb75b4cf8825edb4fa338eac54138
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180493"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-22-december-2018"></a>Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 22 (2018 年 12 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]


このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 22 の新機能または変更された機能について説明します。 このバージョンは、7.0.5095 のビルド番号を持ちます。

### <a name="dynamics-365-october-18-release-notes"></a>Dynamics 365 2018 年 10 月リリース ノート

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424). あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="platform-update-22-bug-fixes"></a>プラットフォーム アップデート 22 のバグ修正プログラム

プラットフォーム更新 22 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://go.microsoft.com/fwlink/?linkid=2037790)を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化

プラットフォーム更新 22 では、プラットフォーム拡張機能の 3 番目の波を使用できます。 詳細については、[プラットフォーム拡張機能の波 3](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/platform-extensibility3) を参照してください。

## <a name="export-up-to-1-million-rows-to-excel"></a>最大 100 万行を Excel にエクスポート

Excel へのエクスポート機能は、Finance and Operations のグリッドから最大 100 万行をエクスポートできるように構成できるようになりました。以前の 10,000 行の制限から大幅に上昇しました。 既定では、エクスポート制限は 50,000 行に設定されていますが、クライアント パフォーマンス オプション ページからシステム管理者が 100 万行までエクスポート制限を調整できます。

## <a name="improved-usability-of-the-navigation-pane"></a>ナビゲーション ウィンドウの使いやすさの向上

ナビゲーション ウィンドウは、お気に入り、最近開いたページや、ークスペース、特にメイン メニューへのアクセスを提供する Finance and Operations で使用頻度の高いナビゲーション メカニズムです。 その使用率の高さのため、使い勝手を向上させるために、いくつかの方法でナビゲーション ウィンドウが強化されました。 これらの変更は、プラットフォーム Update 22 以降で使用できます。 詳細については、[ナビゲーション ウィンドウの使いやすさが向上](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/updated-navigation-pane)を参照してください。

## <a name="restyled-personalization-toolbar"></a>個人用設定ツールバーの再編成

個人用設定ツールバーがプラットフォーム更新 22 で再編成され、ユーザーが Finance and Operations でエクスペリエンスを簡単にカスタマイズできるようになりました。 次の変更が加えられました。

- 各個人用設定ツールの名前がアイコンと共に表示されるようになったため、ユーザーが使おうと思っているツールをすばやく認識できます。
- 現在のツールを使用する方法についての説明も表示され、目的の個人用設定を行う方法を理解するのに役立ちます。
- ツールバーの一番左にある特定の領域にドラッグ アンド ドロップすることで、個人用設定ツールバー全体を画面内で移動できます。 これにより、ユーザーは以前はツールバーによって見えにくかった要素をカスタマイズできます。

次の画像は、プラットフォーム更新 22 より前の個人用設定ツールバーの表示を示しています。

![プラットフォーム更新 22 より前の個人用設定ツールバー](media/oldPersonalizationToolbar.png "プラットフォーム更新 22 より前の個人用設定ツールバー")

次の画像は、プラットフォーム更新 22 以降の個人用設定ツールバーの表示を示しています。

![プラットフォーム更新 22 以降の個人用設定ツールバー](media/restyledPersonalizationToolbar.png "プラットフォーム更新 22 以降の個人用設定ツールバー")

## <a name="optimized-is-one-of-filtering-experience"></a>「次の値のいずれか」のフィルタリング結果を最適化

「次の値のいずれか」フィルター演算子は、フィルター ウィンドウおよびグリッド ヘッダーのドロップダウン リストを使用する場合にほとんどのフィールドで使用できます。 この演算子により、複数の異なる値に基づいてフィールドをフィルター処理できます。 「次の値のいずれか」演算子の新機能と向上したエクスペリエンスはプラットフォーム更新 22 で利用可能です。 詳しくは、[「次の値のいずれか」のフィルタリング結果の最適化](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering)をご覧ください。

## <a name="paste-lists-from-excel-into-filter-fields-with-the-is-one-of-operator"></a>"次の値のいずれか" 演算子を使って Excel からフィルター フィールドにリストを貼り付け

一部のタスクでは、Finance and Operations でデータのフィルター処理に使用する値の一覧が Excel に表示されることがあります。 たとえば、財務ユーザーは、システムで追加の調査を必要とする伝票のセットをレポートから特定している可能性があり、このユーザーが Excel から Finance and Operations のフィルター フィールドに直接リストをコピーできると最適な場合があります。

プラットフォーム更新 22 以降では、フィルター ウィンドウおよびグリッド列フィルターの「次の値のいずれか」演算子が、フィルター フィールドに直接貼り付けることができるように、Excel からコピーされたリストを認識するようになりました。 これには、Excel のさまざまな行と列からコピーされた値のコレクションが含まれます。 この機能の詳細については、["次の値のいずれか" 演算子を使用して Excel からフィルター フィールドに一覧を貼り付ける](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/paste-filter-lists-from-excel)を参照してください。

## <a name="batch-job-to-handle-sql-index-defragmentation"></a>SQL インデックスの最適化を処理するバッチ ジョブ
プラットフォーム更新プログラム 22 では、断片化したインデックスを再構築する新しいシステム バッチ ジョブが導入されました。 インデックスの断片化により、固有のシナリオでパフォーマンスが著しく低下します。 断片化の問題に対処し、データベースを最高のパフォーマンス状態に維持するため、このバッチ ジョブはスケジュールされた時間に定期的に激しく断片化したインデックスを再構築します。 既定では、そのジョブは毎日現地時間の午前 3:00 に最大 2 時間実行されるようにスケジュールされます。 再構築する必要がある断片化されたインデックスが多くないとバッチ ジョブが判断した場合は早期に完了します。  

詳細については [SQL インデックスの最適化を処理するバッチ ジョブ](../../dev-itpro/sysadmin/batch-job-SQL-defragmentation.md) を参照してください。

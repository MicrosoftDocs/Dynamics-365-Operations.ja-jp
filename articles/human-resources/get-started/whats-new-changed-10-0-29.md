---
title: Dynamics 365 Human Resources 10.0.29 (2022 年 10 月) の新機能または変更された機能
description: この記事では、Microsoft Dynamics 365 Human Resources バージョン 10.0.29 プレビュー リリースの新機能または変更された機能について説明します。
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0e51e92a971733dee501986d093e4066c2b172eb
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/03/2022
ms.locfileid: "9223823"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-10029-october-2022"></a>Dynamics 365 Human Resources 10.0.29 (2022 年 10 月) の新機能または変更された機能

[!include [banner](../../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Human Resources バージョン 10.0.29 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1326 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 8 月
- **リリースの一般提供 (自己更新)**: 2022 年 9 月
- **リリースの一般提供 (自動更新)**: 2022 年 10 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能名 | 開始する | リリース状態 |
|----|----|----|
| 場所の所有者の指定 | この機能を使用すると、システム管理者が場所 (住所) の所有者を指定できます。 | 既定 |
| 給付金通知 | このプレビュー機能により、新規採用の登録、オープン登録、および対象となるライフ イベントのシナリオが該当する従業員に電子メールの通知およびアラームを送信できます。 複数のメール テンプレートを作成および設定し、**給付金** ワークスペースと **作業者の給付金** ページを使用して通知を送信することができます。 また、通知およびリマインダーの履歴を追跡することもできます。 | プレビュー |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) には記載されません。

| 機能名 | 詳細 |
|--------------|------------------|
| タスク管理 | Dataverse 経由で通知オプションをサポートするための追加のエンティティが作成されました。 HCMProcessTaskAssignment には、割り当てタイプ、法人、割り当てられた作業者の名前、割り当てられた作業者の人員番号、および割り当てられた作業者の基本電子メール アドレスが含まれます。 すべての業務プロセス タイプが、単一のエンティティ (オンボード、オフボード、および移行) に含まれています。 タスクがグループに割り当てられている場合、そのグループの各メンバーはエンティティ内の 1 行になります。 タスク管理カレンダーのデモ データは、2030 年まで更新されました。 |
| セキュリティのコンフィギュレーション | <p>次のセルフサービス ロールがセキュリティ コンフィギュレーションに追加され、スタンドアロンの HR セルフサービス ロールにマップされます。</p><ul><li>セルフ サービス マネージャー</li><li>セルフ サービス従業員</li><li>セルフサービス契約社員</li></ul><p>これらの領域へのアクセスにはチーム メンバーのライセンスが必要なため、セルフサービス ロールにはタイム シートエントリも経費も **含まれません**。 前のリストのロールは、HR セルフサービス ライセンスで使用する必要があります。 |
| ライフ イベント | 福利厚生管理のライフ イベント エクスペリエンスに対して複数の更新が行われました。 | 

## <a name="features-on-by-default-in-this-release"></a>このリリースで、既定で有効になる機能

次の表に、バージョン 10.0.29 で既定で有効になる機能の一覧を示します。 有効にした機能のほとんどは機能管理で自動的にオフにできます。 今後、顧客が最新の機能を確実に使えるよう、自動的に有効にした機能の一部が機能管理から削除され、必須になる可能性があります。 これにより、現在の機能を追加する機能に機能拡張を構築できます。 必要不可欠と判断される場合を除き、1 年未満の機能が自動的に有効になることはありません。 

| 機能名 | 機能の追加日 | 機能状態 | モジュール |
| ---- | ---- | ---- | ---- |
| タスク管理 | 2022 年 3 月 31 日 | 既定で有効 | Human Resources |
| 会社間報酬を使用した、未来の日付の作業者の移動 | 2019 年 8 月 31 日 | 既定で有効 | Human Resources |
| 有効な職位をフィルター処理 | 2020 年 1 月 6 日 | 既定で有効 | Human Resources |
| 管理者は、拡張レポートでパフォーマンス関連情報を表示できます | 2021 年 4 月 29 日 | 既定で有効 | Human Resources |
| 人事管理のユーザー エクスペリエンスの改善 | 2022 年 3 月 31 日 | 既定で有効 | Human Resources |
| ジョブごとに複数の報酬レベルを構成する | 2022 年 3 月 31 日 | 必須 | Human Resources |
| 業務評価を印刷する | 2022 年 3 月 31 日 | 既定で有効 | Human Resources |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Finance 10.0.29 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.29 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) を参照してください。

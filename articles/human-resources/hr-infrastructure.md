---
title: Dynamics 365 Human Resources インフラストラクチャ マージ - リリース 10.0.25 更新
description: このトピックでは、インフラストラクチャ マージの最初のサイクルとなる Microsoft Dynamics 365 Human Resources のリリース 10.0.25 についてご紹介します。
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a80bedd0224f1e31dfec4e9f4c39ad1ed75d7f2f
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024570"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources インフラストラクチャ マージ - リリース 10.0.25 更新

10.0.25 リリースでは、インフラストラクチャ マージの最初のサイクルが搭載されています。 インフラストラクチャの統合では、Microsoft Dynamics 365 Human Resources は Finance and Operations のインフラストラクチャに統合されます。 しかし、 Dynamics 365 Finance や Dynamics 365 Supply Chain Management のように、独立したアプリケーションとしてのライセンスは継続されます。 インフラストラクチャ マージの詳細については、 [Dynamics 365 Human Resources インフラストラクチャ マージ FAQ](../human-resources/hr-infrastructure-merge-faq.md) を参照してください。

この統合により、次の方法で Human Resources ユーザーに整合性が確保されます。

- [環境の管理と統合は、人事および財務と運用アプリの間で一貫しています。](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Lifecycle Services の Microsoft Dynamics 環境管理、問題検索、および Regression Suite Automation Tool。
    - 1 つのコード ベースがあり、定期的な One Version アップデート プロセスの一環として、Human Resources の新機能がリリースされます。
    - アップグレード、更新、修正プログラムの環境への適用方法は一貫しています。

- [機能拡張オプションが強化されました。](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Microsoft Power Platform tools は引き続き使用でき、必要に応じて拡張できます。
    - フォーム、テーブル、メソッド、アプリケーション プログラミング インターフェース (API) などで機能を拡張することができます。
    - エンティティを作成、拡張できます。

    使用できる拡張機能オプションの詳細については、[Dynamics 365 の拡張機能の概要](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md)を参照してください。

- [Dynamics 365 で 1 セットの人事管理機能を作成します。](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    10.0.25 のリリースでは、Human Resources のみに存在していた機能が Finance and Operations のインフラストラクチャで利用できるようになりました。 顧客が Finance and Operations の環境でこれらの機能を利用するには、機能管理で次の Human Resources 機能を有効にする必要があります。

    | 機能名 | 概要 | リリース状態 | 
    |--------------|----------|----------------| 
    | 勤続年数の計算 | 設定オプションを使用すると、**サービス年** の計算に使用する日付を選択できます。 | 一般に入手可能 | 
    | ワークフロー エクスペリエンスの強化 | この機能により、ワークフローの提出や承認の際のユーザー エクスペリエンスが向上します。 | 一般に入手可能 | 
    | 業務評価を印刷する | パフォーマンス レビューは PDF 形式で印刷できます。 | 一般に入手可能 | 
    | **マネージャー セルフサービス** のカスタム リンク | **マネージャ セルフサービス** の **関連リンク** セクションに表示されるカスタム リンクを作成できます。 | 一般に入手可能 | 
    | 会社間報酬ビュー | ユーザーは、会社を切り替えることなく、すべての法人を対象に **マネージャ セルフサービス** で報酬プランを閲覧することができます。 | 一般に入手可能 | 
    | 職務 \*&dagger; ごとに複数の報酬レベルを構成する | ジョブが複数の報酬レベルに対応しました。 | プレビュー | 
    | タスク管理\* | オンボード、オフボード、切り替えプロセスのチェック リストやタスクを作成することができます。 | プレビュー | 
    | 合理化された従業員の入力 | この機能により、既存の **作業者r** ページに表示される最新のユーザー エクスペリエンスが提供されます。 | プレビュー | 
    | 人事管理のユーザー エクスペリエンスの改善 | 次のセクションの表を参照してください。  | プレビュー | 

\* **人事管理ユーザー エクスペリエンス向上** 機能を使用する前に、この機能を有効にする必要があります。

&dagger; この機能は、有効化した後で無効にすることはできません。

## <a name="human-resource-user-experience-enhancements"></a>人事管理ユーザー エクスペリエンスの向上

| 機能名 | 概要 | 
|--------------|----------| 
| 雇用の削除 | 従業員の雇用を削除できます。 | 
| ジョブ ファミリ | 類似する仕事をしていて、類似するトレーニング、スキル、知識、専門知識を必要とする仕事のグループを追跡することができます。 | 
| 追加の雇用フィールド | **雇用カテゴリ**、**雇用タイプ**、**雇用ステータス** のフィールドが追加されました。 | 
| **雇用されていない作業者** ページ | ページには、雇用レコードのない労働者のリストが表示されています。 | 
| 職位分析コードのユーザーエクスペリエンス更新 | 法人ごとに職位分析コードを割り当てる際のユーザー エクスペリエンスが向上しました。 | 
| **個人管理** ワークスペースの住所変更 | この機能は、**人事管理パラメーター** ページに定義されているように、指定された日数の間に発生したすべての住所変更のカウントを提供します。 | 
| **個人管理** ワークスペースの期限切れレコード | この機能では、証明書、身分証明書、検認、審査、テストなどの期限切れ、または期限が切れる予定のアイテムのリストを提供します。 | 
| **職位階層の検証** ページ | 職位ライン階層での循環参照のチェックが行われます。 | 
| 国固有の給与情報 | 作業者が雇用されている法人の国や地域に応じて、**作業者の雇用** ページに追加の給与計算フィールドが用意されています。 | 
| コンプライアンス レポートの拡張機能 | 追加のレポート オプションは、EEO-1、Vets 4212、OSHA300a に対して使用できます。 | 
| **人員管理** ワークスペースの更新 | 住所変更や期限切れの記録を追跡する更新が行われました。 さらに、新しいタブには、作業者と職位のアクションが一覧表示されます。 | 

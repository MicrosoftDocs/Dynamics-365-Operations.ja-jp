---
title: 人材の更新
description: この記事は、Microsoft Dynamics 365 Talent に関するプロセスと頻度についての情報を提供します。
author: andreabichsel
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: IT Pro
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-11-15
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: 4aca90cf91587168a51a0cfdee5fe61f92de0e6b
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031056"
---
# <a name="talent-updates"></a>人材の更新

Microsoft Dynamics 365 Talent は、継続的な自動サービス更新を提供するサービス (SaaS) としての真のソフトウェアです。 これらの更新には、定期的な更新を含むサービスに対する重要な改良を提供する、アプリケーションとプラットフォーム両方の変更が含まれます。

## <a name="update-policy"></a>更新ポリシー

更新はすべての環境に対して一定の調子でリリースされます。 Talent は、[Microsoft Lifecycle ポリシー](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)に従ってサポートされています。ここでは、製品サポートの使用可能性における一貫した予測可能なガイドラインを提供します。

## <a name="release-cadence"></a>リリースの頻度

Talent の更新は、すべての環境に自動的に適用されます。 Talent には次の 2 つの種類のリリースがあります:

- **サービス更新**: バグ修正および新機能を含む週 1 回の更新。 サービス更新には、リリース時に該当するプラットの更新も含まれます。 プラットフォーム更新がリリースされた時期を把握するには、[表 3: Platform リリース](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases) を参照してください。 毎週の更新は通常水曜日にリリースされます。 毎週の更新についての詳細は、[Dynamics 365 Talent の新機能および変更された機能](https://docs.microsoft.com/dynamics365/talent/whats-new) を参照してください。

    特に断りのない限り、サポートされているすべてのデータセンターが毎週更新されます。 毎週の更新は、通常は水曜日に開始され、日曜日に完了します。 米国、オーストラリア、ヨーロッパ、英国、アジア、およびカナダ地域が毎週の更新プログラムに含まれています。 

- **Common Data Service ソリューションの更新**: これらの更新は、必要に応じて約 6 週間ごとに行われます。 この中には、新規エンティティと Common Data Service の既存のエンティティに対する変更が含まれています。 これらの更新は、週単位の更新と同じ地域に対してリリースされ、すべてのデータ センターを通じてレプリケートされるまでに約 6 週間かかります。 ソリューションび更新は、毎週のサービス更新と一致しない場合もあります。

次の表は、スケジュールの例を示します。

| 週 | 更新タイプ |
| --- | --- |
| 1 | サービス更新 (すべての地域) |
| 2 | サービスの更新 (すべての地域) + ソリューションの更新 (Week 1 地域) |
| 3 | サービスの更新 (すべての地域) + ソリューションの更新 (Week 2 地域) |
| 4 | サービスの更新 (すべての地域) + ソリューションの更新 (Week 3 地域) |
| 5 | サービスの更新 (すべての地域) + ソリューションの更新 (Week 4 地域) |
| 6 | サービスの更新 (すべての地域) + ソリューションの更新 (Week 5 地域) |
| 7 | サービスの更新 (すべての地域) + ソリューションの更新 (Week 6 地域) |
| 8 | サービス更新 (すべての地域) |

> [!NOTE]
> リリースされたすべてのデータセンターで、ソリューションの更新が使用できます。 更新の複製が自動的に行われるのを待機したくない場合は、すべてのデータ センターの任意の環境にこれらの更新を手動で適用することができます。

必要に応じて、次のタイプの修正も用意されています:

- **リビジョン (修正プログラム)**: 週単位のサービス更新プログラムのリリースとは別に、またはその他の方法で発生する可能性のあるバグ修正

- **緊急の修正**: 本質的にスタンドアロンである予防的なおよび李アクティブな修正プログラムには、サイトの問題を解決するためのコンフィギュレーションのみまたはコードの変更が含まれる場合があり、毎週のサービス更新リリースとは別に発生することができます。

リリースは、内部環境で確認、テスト、および検証されます。 ビルドがサインオフされた後、その後、生産に配置されます。

## <a name="exceptions-in-2019"></a>2019 での例外

次の日付は、通常のリリース スケジュールに対する例外です:

| 日 | 説明 |
| --- | --- |
| 11 月 25 日の週 | 更新なし |
| 12 月 16 日の週 | マイナー更新のみ |
| 12 月 23 日の週 | 更新なし |
| 12 月 30 日の週 | 更新なし |

## <a name="communications"></a>通信

Talent の作業の内容と、次の場所でリリースされた機能について検索できます:

- [Dynamics 365 Talent ロードマップ](https://dynamics.microsoft.com/roadmap/talent/)

- [Dynamics 365 リリース プラン](https://docs.microsoft.com/dynamics365/release-plans/)

- [Dynamics 365 Talent での新機能と変更](https://docs.microsoft.com/dynamics365/talent/whats-new)

- [Lifecycle Services (LCS) での問題検索](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (プラットフォームに関連するバグのみ)

- [Talent ブログ](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Talent Yammerコミュニティー](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>サンドボックス環境におけるプレビュー機能

サンドボックス環境でプレビュー機能を検証してから、実働環境で有効にすることができます。 機能の有効化についての詳細は、[機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。

すべての新機能は少なくとも 30 日間、通常は30-60日間、プレビューのままになります。 主な機能は、通常、プレビュー期間に従って毎年 10 月と 4 月に使用可能です。 機能管理ワークスペースに新しい機能が表示されたら、すぐにそれらをオンにすることができます。 一部の機能は既定でオンになっている場合があります。

場合によっては、通常は整数機能が有効になりますが、オフにすることはできません (機能管理ワークスペースなど)。

機能が一般に使用可能になったら、運用環境でオンまたはオフにすることができます。 機能管理ワークスペースは、プレビュー機能が必須になるタイミングを示します。 この日付は、通常、半年のリリース計画に沿って 10 月 1 日または 4 月 1 日になっています。 必須機能を無効にすることはできません。 必須になるまでは、すべての環境で機能を有効または無効にすることができます。

サンドボックス環境またはトライアル環境で機能をプレビューすることを強くお勧めします。 データを使用して新しい機能を完成させるには、現在の実稼働環境またはデータベースのコピーをサンドボックス環境に作成することをお勧めします。

サンドボックス環境のプロビジョニングの詳細については、[Talent プロジェクトのプロビジョニング](provisioning-talent.md#provision-a-talent-project) を参照してください。 テスト環境を削除するには、[テスト ドライブ環境の削除](remove-talent-environment.md#removing-a-test-drive-environment) を参照してください。 

## <a name="report-bugs"></a>バグのレポート

プレビュー機能をテストしたり、新機能を試す間に、期待どおりに機能しない項目が見つかる場合があります。 バグは、[Microsoft Dynamics 365 サポート](https://dynamics.microsoft.com/support/) を通じて報告してください。

## <a name="see-also"></a>参照

- [Dynamics 365 および Power Platform リリース プラン](https://docs.microsoft.com/dynamics365/release-plans)
- [Dynamics 365 Talent での新機能と変更](https://docs.microsoft.com/dynamics365/talent/whats-new)
- [ソフトウェアのライフサイクル ポリシー](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

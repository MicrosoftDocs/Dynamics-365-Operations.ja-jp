---
title: 更新プロセス
description: Microsoft Dynamics 365 Human Resources は、アプリケーションとプラットフォームの変更のための、継続的な自動サービス更新を提供するサービス (SaaS) としての真のソフトウェアです。
author: andreabichsel
manager: tfehr
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bb5f7dc17c8f4f3a54bd285cb55088f2176db4a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113235"
---
# <a name="update-process"></a>更新プロセス

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources は、継続的な自動サービス更新を提供するサービス (SaaS) としての真のソフトウェアです。 これらの更新には、定期的な更新を含むサービスに対する重要な改良を提供する、アプリケーションとプラットフォーム両方の変更が含まれます。

## <a name="update-policy"></a>更新ポリシー

更新はすべての環境に対して一定の調子でリリースされます。 人事管理は、[Microsoft Lifecycle ポリシー](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)に従ってサポートされていて、製品サポートの使用可能性における一貫した予測可能なガイドラインを提供します。

## <a name="release-cadence"></a>リリースの頻度 

人事管理の更新は、すべての環境に自動的に適用されます。 人事管理には次の 2 つの種類のリリースがあります:

- **サービスの更新**: バグ修正および新機能を含む、隔週でリリースされる更新プログラム。 サービス更新には、リリース時に該当するプラットの更新も含まれます。 プラットフォーム更新がリリースされた時期を把握するには、[表 3: Platform リリース](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases) を参照してください。 隔週の更新では、地域全体に段階的に展開されます。 隔週の更新についての詳細は、[Dynamics 365 Human Resources の新機能および変更された機能](hr-admin-whats-new.md) を参照してください。

    特に断りのない限り、サポートされているすべてのデータ センターが隔週で更新されます。 米国、オーストラリア、ヨーロッパ、英国、アジア、カナダが隔週の更新プログラムに含まれています。 

- **Dataverse ソリューションの更新**: これらの更新は、必要に応じて約 6 週間ごとに行われます。 この中には、新規エンティティと Dataverse の既存のエンティティに対する変更が含まれています。 これらの更新は、隔週の更新と同じ地域に対してリリースされ、すべてのデータ センターを通じてレプリケートされるまでに約 6 週間かかります。 ソリューションの更新は、隔週のサービス プログラムの更新と一致しない場合もあります。

> [!NOTE]
> リリースされたすべてのデータセンターで、ソリューションの更新が使用できます。 更新の複製が自動的に行われるのを待機したくない場合は、すべてのデータ センターの任意の環境にこれらの更新を手動で適用することができます。

必要に応じて、人事管理では次のタイプの修正も用意されています:

- **リビジョン（修正プログラム）**: 隔週のサービス更新プログラムのリリースとは別に、またはその他の方法で実行される可能性のあるバグ修正

- **緊急の修正**: 本質的にスタンド アロンである事前対応および事後対応の修正プログラムには、サイトの問題を解決するための構成のみ、またはコードの変更が含まれる場合があり、隔週のサービス更新のリリースとは別に発生することができます。

リリースは、内部環境で確認、テスト、および検証されます。 ビルドがサインオフされた後、その後、生産に配置されます。

## <a name="release-cadence-exceptions-in-2020"></a>2020 年のリリース 間隔の例外

休日を考慮した、2020 年 11 月と 12 月のリリース スケジュールは次のとおりです:

- 11 月リリース: 11 月 2 日 - 11 月 13 日
- 12 月リリース: 11 月 30 日 - 12 月 11 日
 
2 週間のリリース頻度は、2021 年 1 月 11 日に通常どおり再開します。

## <a name="communications"></a>通信

人事管理の作業の内容と、次の場所でリリースされた機能について検索できます:

- [Dynamics 365 Human Resources ロードマップ](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365 リリース プラン](https://docs.microsoft.com/dynamics365/release-plans/)

- [Dynamics 365 Human Resources での新機能と変更](hr-admin-whats-new.md)

- [Lifecycle Services (LCS) での問題検索](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (プラットフォームに関連するバグのみ)

- [人事管理のブログ](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [人事管理 Yammer コミュニティ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>サンドボックス環境におけるプレビュー機能

サンドボックス環境でプレビュー機能を検証してから、実働環境で有効にすることができます。 機能の有効化についての詳細は、[機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。

すべての新機能は少なくとも 30 日間、通常は30-60日間、プレビューのままになります。 主な機能は、通常、プレビュー期間に従って毎年 10 月と 4 月に使用可能です。 機能管理ワークスペースに新しい機能が表示されたら、すぐにそれらをオンにすることができます。 一部の機能は既定でオンになっている場合があります。

場合によっては、通常は整数機能が有効になりますが、オフにすることはできません (機能管理ワークスペースなど)。

機能が一般に使用可能になったら、運用環境でオンまたはオフにすることができます。 機能管理ワークスペースは、プレビュー機能が必須になるタイミングを示します。 この日付は、通常、半年のリリース計画に沿って 10 月 1 日または 4 月 1 日になっています。 必須機能を無効にすることはできません。 必須になるまでは、すべての環境で機能を有効または無効にすることができます。

サンドボックス環境またはトライアル環境で機能をプレビューすることを強くお勧めします。 データを使用して新しい機能を完成させるには、現在の実稼働環境またはデータベースのコピーをサンドボックス環境に作成することをお勧めします。

サンドボックス環境のプロビジョニングの詳細については、[人事管理プロジェクトのプロビジョニング](hr-admin-setup-provision.md) を参照してください。 テスト環境を削除するには、[インスタンスの削除](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment) を参照してください。 

## <a name="report-bugs"></a>バグのレポート

プレビュー機能をテストしたり、新機能を試す間に、期待どおりに機能しない項目が見つかる場合があります。 バグは、[Microsoft Dynamics 365 サポート](https://dynamics.microsoft.com/support/) を通じて報告してください。

## <a name="see-also"></a>参照

[Dynamics 365 および Power Platform リリース プラン](https://docs.microsoft.com/dynamics365/release-plans)</br>
[Dynamics 365 人事管理の新機能および変更された機能](hr-admin-whats-new.md)</br>
[ソフトウェアのライフサイクル ポリシー](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
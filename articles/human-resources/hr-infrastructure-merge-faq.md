---
title: Dynamics 365 Human Resources インフラストラクチャ統合 FAQ
description: この記事では、Microsoft Dynamics 365 Human Resources および財務と運用アプリのインフラストラクチャの統合に関してよく寄せられる質問に回答します。
author: twheeloc
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32698d887b4d228ded588984b09068e3e2fef9a4
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702070"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources インフラストラクチャ統合 FAQ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Dynamics 365 Human Resources とは

Microsoft Dynamics 365 Human Resources は、HR チームが組織の機敏性を高め、従業員の経験を変革し、HR プログラムを最適化して、人とビジネスが繁栄できる職場を作るのに役立つツールを提供します。 Dynamics 365 Human Resources の詳細については、[Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/) を参照してください。

- **従業員エクスペリエンスを変換します。** エンゲージメントと成長を促進する接続されたセルフサービス エクスペリエンスを通じてマネージャーと従業員に権限を与えることで、上位担当者を維持します。
- **HR プログラムを最適化します。** 運用コストを削減し、人を中心に考えた休暇、時間、福利厚生、および報酬管理の各プログラムを作成します。
- **組織の機動性を高めます。** Dataverse と Microsoft Power Platform を使用して人材データを一元化し、Dynamics 365 Human Resources を簡単に拡張することで、HR がビジネスに必要な機敏さをもって機能するようにします。
- **従業員に関する分析情報を得ます。** 任意のデバイスで利用できる豊富なダッシュボードで従業員のデータを分析および視覚化する機能により、データ駆動型の意思決定を行います。

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>インフラストラクチャ統合の価値と利点

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources インフラストラクチャ統合とは ?

Dynamics 365 の 2 つの異なるインフラストラクチャには、現在 2 つの異なる HR 機能セットがあります。

- **Dynamics 365 Human Resources**: 独立したインフラストラクチャ上で実行されるスタンドアロン アプリ。 このアプリケーションが起動された時点で、インフラストラクチャは他の Dynamics 365 運用アプリから分離されました。 顧客はこのアプリを使用して、組織の機敏性を高め、HR プログラムを最適化して従業員のエクスペリエンスを変換し、従業員に関する分析情報を得ることができます。
- **HR モジュール** – 以前は Unified Operations ライセンス最小在庫管理単位 (SKU) の一部であった機能のレガシ セット。 HR モジュールはすべての運用アプリと同様に、財務と運用インフラストラクチャ上で実行されます。 これらのアプリには、Dynamics 365 Finance、Dynamics 365 Project Operations、および Dynamics 365 Supply Chain Management が含まれます。 顧客は、Dynamics 365 Finance または Dynamics 365 Supply Chain Management の一部として HR 機能を受け取ります。

過去 3 年間で、Microsoft は HR モジュールに新しい機能や拡張機能を追加していません。 代わりに、ロードマップへの投資は Dynamics 365 Human Resources アプリに集中しています。

これら 2 つの機能セットを同じインフラストラクチャに統合することで、顧客は次のようなメリットを得ることができます。

- 過去 3 年間に Dynamics 365 Human Resources に追加された拡張機能 (休暇と欠勤、福利厚生の管理、報告など)。
- Microsoft Power Platform による拡張機能の向上と、ビジネスロジックを拡張してページをパーソナライズする機能。
- アプリケーション ライフサイクル管理 (ALM)、Lifecycle Services、地理的な可用性などの点で一貫し改善された展開、更新、および保守。
- エンジニアリング チームが共有サービス、ツール、および削減されたプラットフォーム コストを使用することで、さらなる技術革新が実現します。

この移行は、現在 Dynamics 365 Human Resources または従来の HR モジュールを使用している顧客に影響します。

## <a name="glossary-of-terms-used-in-this-faq"></a>この FAQ で使用される用語集

- **Dynamics 365 Human Resources** – HR 機能を市場に提供する現在および将来の製品。
- **HR モジュール** – 以前に Unified Operations オファリングでライセンス供与されていたレガシ機能のセット。 この機能は、顧客が Dynamics 365 Finance または Dynamics 365 Supply Chain Management を所有している場合に有効になります。
- **財務と運用のインフラストラクチャ** – Dynamics 365 Finance、Dynamics 365 Supply Chain Management、および Dynamics 365 Project Operations などの運用ポートフォリオで使用される開発アーキテクチャ。 このインフラストラクチャは、今後使用されるインフラストラクチャです。 この FAQ では、*マージされたインフラストラクチャ* という用語は、財務と運用の環境を指します。
- **人事管理インフラストラクチャ** – 以前 Dynamics 365 Human Resources アプリに使用された開発アーキテクチャ。 インフラストラクチャ統合プロジェクトにより、Dynamics 365 Human Resources を財務と運用インフラストラクチャにもたらします。 スタンドアロンのインフラストラクチャは廃止されます。

## <a name="general-questions-about-the-infrastructure-merge"></a>インフラストラクチャ統合に関する全般的な質問

### <a name="will-customers-lose-any-features-or-capabilities"></a>顧客は機能を失いますか?

私たちの目標は、この移行が顧客に与える影響を最小限に抑えることです。 機能が削除されることはありません。 Dynamics 365 Human Resources と HR モジュールの間には、機能的な同等性があります。 機能が両方のインフラストラクチャに存在する場合、Dynamics 365 Human Resources のエクスペリエンスが使用されます。

### <a name="will-the-user-experience-change"></a>ユーザー エクスペリエンスは変化しますか?

ユーザー エクスペリエンスは、標準の Dynamics 365 プラットフォーム エクスペリエンスと一致します。 ダッシュボードとメニューの一般的なエクスペリエンスは同じままですが、Dynamics 365 Finance アプリのエクスペリエンスと連携します。 ナビゲーションには、モジュールとワークスペースの両方が含まれます。お気に入りを許可することもできます。 **人事管理** および **人員** などの Dynamics 365 Human Resources ワークスペースは、財務と運用インフラストラクチャに統合されます。 将来、新機能は機能管理を通じて配信されます。顧客は新しい機能を表示し、どの機能を使用するかを決定します。 詳細については、[機能管理の概要](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)および[ユーザー インターフェイスのドキュメント](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json) を参照してください。

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Dynamics 365 Human Resources インフラストラクチャの統合はいつ完了しますか?

インフラストラクチャの統合は段階的に展開され、顧客が必要なステップを計画して完了するための時間を提供します。 Dynamics 2021 のリリース サイクル 2 で機能を展開しました。 2022 リリース サイクル 2 の終わりまでに、このプロジェクトのすべての製品開発作業を完了する予定です。 タイムラインは変更される可能性があります。 最新情報については、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance) を参照してください。

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>インフラストラクチャ統合を支援するために利用できるトレーニングとリソースは何ですか?

インフラストラクチャ統合の各ステップを詳細に説明するドキュメントが提供されます。 顧客とパートナーの円滑な移行を図る上で必要なトレーニング リソース (ビデオやワークショップなど) を提供します。

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>インフラストラクチャ統合の完了後、開発機能に変化はありますか?

開発機能の詳細については、[ホーム ページの開発とカスタマイズ](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md)を参照してください。

## <a name="feature-availability-questions"></a>利用可能な機能についての質問

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>LinkedIn タレント ハブの統合は、財務と運用のインフラストラクチャで機能しますか?

いいえ、LinkedIn タレント ハブは、統合されたインフラストラクチャの一部にはなりません。 パブリック アプリケーション プログラミング インターフェイス (API) は、採用および申請者追跡ソリューションとの統合を構築するために使用できます。 LinkedIn タレント ハブを使用する予定の顧客は、Microsoft パートナーと連携して、提供される API を使用して統合する必要があります。 申請者追跡システム (ATS) 統合 API の詳細については、[申請者追跡システム統合 API の概要](./hr-admin-integration-ats-api-introduction.md)を参照してください。

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>統合後、現在 Dynamics 365 Human Resources でのみ使用できる機能 (休暇管理や福利厚生管理など) を使用できますか?

はい。 すべての Dynamics 365 Human Resources アプリケーション機能が、財務と運用インフラストラクチャに提供されます。 機能は、段階的なアプローチで使用できます。 統合されたインフラストラクチャの使用可能な機能に関する最新の情報については、定期的に[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance)を参照してください。

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>インフラストラクチャ統合が完了した後、Dynamics 365 Human Resources と Ceridian との統合は利用可能ですか?

Ceridian は、給与 API を利用する Dynamics 365 Human Resources との V2 統合を作成中です。 Dynamics 365 Human Resources に現在存在するファイル ベースの統合は、財務と運用のインフラストラクチャに移行されません。 詳細については、[給与 API の概要](./hr-admin-integration-payroll-api-introduction.md)を参照してください。

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>申請者追跡や、従業員の機能のオンボード/オフボードは含まれますか?

以前のリリースでは、パートナーや顧客が人事管理との ATS 統合を作成できる ATS 統合 API を作成しました。 ATS 関連の追加機能は、2022 サイクル 1 で使用可能になりました。 これらの API は、今後のリリースでも引き続き強化される予定です。

現在財務と運用のインフラストラクチャに存在する HR 機能には、Dynamics 365 Human Resources に存在しない採用管理機能がいくつか含まれています。 インフラストラクチャ統合が完了すると、この機能は人事管理のすべての顧客が利用できるようになります。 この機能により、ライトウェイト ATS 機能が提供されます。 ただし、今後この機能を拡張する予定はありません。 より高度な機能を必要とする顧客は、パートナー ATS 統合を活用できます。 ATS 統合 API の詳細については、[申請者追跡システム統合 API の概要](./hr-admin-integration-ats-api-introduction.md)を参照してください。

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Dynamics AX 2012 アップグレード ツールを使用して、AX 2012 の HR モジュールを Dynamics 365 Human Resources アプリにアップグレードしますか?

はい。 Dynamics AX 2012 から Dynamics 365 Human Resources へのアップグレードは、Dynamics 365 Finance や Dynamics 365 Supply Chain Management など、他の Dynamics 365 運用アプリの最新バージョンへのアップグレードに使用されるのと同じアップグレード パスとツールに従います。

財務と運用インフラストラクチャへの移行の詳細については、[人事管理の顧客移行に関する FAQ](./customer-migration.md) を参照してください。

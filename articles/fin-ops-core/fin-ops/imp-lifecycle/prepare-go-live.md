---
title: Go Live の準備
description: この記事では、財務と運用アプリの Go-Live に向けた準備方法に関するガイダンスを提供します。
author: ClaudiaBetz-Haubold
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 23bf539570fa8d7f9115f3393f212ac8ee60835d
ms.sourcegitcommit: ed8ce31c45f35ea616ee48806149700f00f9d322
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/07/2022
ms.locfileid: "9126521"
---
# <a name="prepare-for-go-live"></a>Go Live の準備

[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリの Go-Live に向けた準備方法に関するガイダンスを提供します。

運用環境がライブ運用に使用されるようにするため、Microsoft はソリューションの準備が整い、Microsoft との Go-live 準備完了レビューの一部としてプロジェクトの準備状況が検証された後に、運用インスタンスをプロビジョニングします。 ご利用のサブスクリプションでの環境の詳細については、[ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) を参照してください。

Go-live に関する一般的な質問への回答については、[Go-live に関するよく寄せられる質問](go-live-faq.md)を参照してください。

次の表に、Go-Live プロセスの重要な手順の一覧を示します。

| ステップ | 期間/時 | 誰 | 摘要 |
|---|---|---|---|
| 前提条件の検証 | プロジェクトではテスト フェーズの終了に近い段階で、Go-live レビューを計画しています。 | 顧客/パートナー | 詳細については、[Go-live 準備完了レビューの前提条件](#prerequisites)セクションを参照してください。 |
| Microsoft による Go-live 準備完了レビュー | Go-live の 4 週間前まで | 顧客/パートナーは、FastTrack for Dynamics 365 実装ポータルでレビュー質問に対する回答を送信します。 Microsoft FastTrack は、レビュー レポートを提供します。 | 詳細については、[Microsoft による Go-live 準備完了レビュー](#readiness) セクションを参照してください。 |
| Microsoft による Go-Live レビュー ワークショップ (対象プロジェクトのみ) | このワークショップは、Go-live 準備完了レビューの一部です。 | Microsoft FastTrack とそのプロジェクト チーム | この手順は、[FastTrack 契約](/dynamics365/fasttrack/eligibility)がある対象プロジェクトのみに適用されます。 ワークショップに関する詳細については、[Go-live 準備完了ワークショップ](/dynamics365/fasttrack/go-live-workshops)を参照してください。 |
| 運用配置 | Go-live 準備完了レビューの完了後すぐに運用配置を開始できます。 配置がトリガーされると、運用配置に約 30 分かかります。 | 顧客/パートナーは、Microsoft Dynamics Lifecycle Services (LCS) への配置をトリガーします。 | Go-live レビューが正常に完了すると、運用環境の **構成** ボタンが有効になります。 このボタンを選択すると、[運用配置がトリガーされます](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)。 |
| 配置可能パッケージのインストール | 平均 30 分 | 顧客/パートナー | [運用環境への更新の導入](../../dev-itpro/deployment/updateenvironment-newinfrastructure.md#promote-an-update-to-production-environments)の指示に従います。 このパッケージには、[オールインワン配置可能パッケージ](../../dev-itpro/dev-tools/aio-deployable-packages.md)内に統合されたすべてのモデルとバイナリを含める必要があります。 |
| 運用へのデータ移行 | 期間/時間は使用する方法によって異なります。 | 顧客/パートナー | |
| 切替活動 | 期間/時間はプロジェクトに依存します。 | 顧客/パートナー | |
| Go-live | | 顧客/パートナー | |

## <a name="go-live-readiness-review-prerequisites"></a><a name="prerequisites"></a>Go-live 準備完了レビューの前提条件

プロジェクト チームは、ソリューションの準備完了を検証する必要があります。 Microsoft による Go-live 準備完了レビューを開始する前に、次の前提条件を満たす必要があります。 Microsoft による Go-live 準備完了レビューが正常に完了した後に、運用環境を配置できます。

- ユーザー受け入れテスト (UAT) とパフォーマンス テストは、レベル 2 (以上) の環境で完了済またはほぼ完了しています。 UAT またはパフォーマンス テストには、レベル 1 環境を使用しないでください。 詳細については、[レベル 1 対レベル 2 以上](environment-planning.md#tier-1-vs-tier-2-and-higher)を参照してください。 トランザクション量に応じた、正しいサンドボックス環境レベルの特定方法については、[正しいレベル 2 以上の環境を選択する](environment-planning.md#selecting-the-correct-tier-2-or-higher-environment)を参照してください。

    UAT フェーズ中に、実装したすべての業務プロセステストと、実施した任意のカスタマイズをテストします。

    - テスト ケースは、要件の範囲全体をカバーする必要があります。
    - 移行したデータをテストに使用します。 このデータには、最終データではない場合でも、マスター データと期首残高が含まれている必要があります。
    - テストには、既定のロールおよびユーザーに割り当てられたカスタム ロールを含む、正しいセキュリティ ロールを使用します。
    - ソリューションが会社別および業界別の規制要件に準拠していることを確認します。
    - 顧客からのサインオフを取得します。

    パフォーマンス テストは、ソリューションの準備完了を検証するのに不可欠な部分です。 推奨事項の詳細なガイダンスについては、[パフォーマンス テスト Techtalks](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/performance-testing-in-microsoft-dynamics-365-techtalk-series) を参照してください。

- Go-live 用に計画された環境バージョンは、[ソフトウェアのライフサイクル ポリシー](../../dev-itpro/migration-upgrade/versions-update-policy.md)に準拠しています。 Commerce Scale Units (CSU) を使用する場合、CSU バージョンは環境バージョンと同期している必要があります。 詳細については、[コンポーネントの依存関係](/commerce/arch-component-versioning.md#component-dependencies)を参照してください。
- 主要な顧客チーム メンバーが LCS プロジェクトに追加されました。
- 運用環境の配置に使用する汎用サービス アカウントが LCS に追加されました。
- Go-live に必要なすべてのライセンスが、正しいテナントで購入されました。
- すべてのライセンスが購入された後、最終的なサブスクリプション見積もりツールが LCS にアップロードされ、有効化されます。 詳細については、[Lifecycle Services (LCS) のサブスクリプション見積もりツール](../../dev-itpro/lifecycle-services/subscription-estimator.md)を参照してください。
- カスタマイズ分析レポート (CAR) を実行し、重大な問題を解決されました。 詳細については、 [カスタマイズ分析のレポートt (CAR)](../../dev-itpro/dev-tools/customization-analysis-report.md)を参照してください。
- LCS の Go-live 日付は、対象とする Go-live 日付を正しく表します。 この日付は、エンド ユーザーがカットオーバー活動ではなく、ライブ運用を開始する日付です。
- [LCS 手法](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies)の関連タスクおよびフェーズはすべて完了しています。 運用は、テスト フェーズを含むすべてのフェーズが完了した後にのみ配置できます。 LCS でフェーズを完了するには、まずそのフェーズで必要なすべてのステップを完了する必要があります。 フェーズにあるすべてのタスクが完了したら、そのフェーズ全体を完了することができます。 変更する必要がある場合、常に後からフェーズを再オープンすることができます。 ステップを完了するプロセスは 2 つの部分で成り立っています。

    - フィット ギャップ解析または UAT など、実際の作業を行います。
    - LCS 手法の対応するステップを完了としてマークします。

    実装の進捗状況に応じて手法のステップを完了します。 最後まで待たないでください。

## <a name="go-live-readiness-review-with-microsoft"></a><a name="readiness"></a>Microsoft による Go-live 準備完了レビュー

すべての財務と運用アプリの顧客は、運用環境を展開する前に [Microsoft FastTrack for Dynamics 365](/dynamics365/fasttrack/) チームで、Go-live 準備完了レビューを完了する必要があります。 レビューの主要な目的は、プロジェクトの準備完了を評価し、円滑で正常な Go-live エクスペリエンスを支援することです。 LCS プロジェクト ユーザーは、LCS 日付に基づいて、Go-live 準備完了レビューに関する電子メール通知を受け取ります。

レビューでは、初期レポートに最大 3 営業日、さらにリスク軽減が必要な場合は追加で時間を要する場合があります。 このレビューを開始する適切な時間を決定して、Go-Live タイムラインに間に合うようにします。

ほとんどのプロジェクトに関しては、Go-live 準備完了レビューは、FastTrack for Dynamics 365 実装ポータルで行われます。

> [!Note]
> FastTrack for Dynamics 365 実装ポータルを使用しない **2 つの例外** があります:
> - **[米国 (US) 政府機関向けコミュニティ クラウド (GCC)](../../dev-itpro/deployment/us-gcc-deployment.md)** に入っているプロジェクトです。 [Go-live チェックリスト](https://aka.ms/d365fogolivechecklist)をダウンロードし、必要事項をご記入の上、<d365fogccglr@microsoft.com> まで電子メールで送信してください。 電子メールには、顧客からの主な関係者と実装パートナーを必ず含めます。 Microsoft FastTrack がプロジェクトをレビューし、フォローアップします。
> - 既に運用しているプロジェクトで、運用ソリューションを新しいテナントに移動する予定だった場合は、ソリューションが変更されていなければ、新たに Go-live 準備完了レビューを完了する必要はありません。 [運用環境を新しいテナントに移動する](../get-started/move-lcs-implementation-project-tenant.md#move-your-production-environment-to-the-new-tenant)で説明されている手順に従い、新しいテナントで生産スロットを有効にします。

### <a name="initiate-the-go-live-readiness-review-in-the-portal"></a>ポータルで Go-live 準備完了レビューを開始する

1. 顧客/パートナーから <d365fogl@microsoft.com> 宛に、以下の内容を記載したメールが送信されます:

    - プロジェクトで Go-live 準備完了レビューを開始する準備が整ったという確認
    - LCS プロジェクト ID の確認
    - **LCS プロジェクトから Go-live 準備完了レビューに参加し、Go-live 準備完了レビュー プロセスのポータルへのアクセスを許可されるユーザーの確認**

    > [!NOTE]
    > レビューに参加している顧客組織からの主要な利害関係者は、ポータルの **レビュー参加者** として選択される必要があります。

2. Microsoft は、要求された LCS プロジェクト ユーザーに対してポータルのアクセス許可を付与し、電子メールに返信することでこのタスクが完了したことを確認します。
3. 顧客/パートナーは、[ポータルのヘルプ記事](https://experience.dynamics.com/FTimplementationportal/help/help-details-page/?id=a275750e-2ffb-eb11-94ef-0022482594cd&searchtxt=)のガイダンスに従ってポータルのレビューを開始します。 ポータルへのアクセス許可を持っているすべてのユーザーは、この記事にアクセスできます。

### <a name="submit-the-review"></a>レビューを提出する

- プロジェクト チームは、レビューのすべての質問に回答する必要があります。 ポータルのレビュー プロセスは、複数ユーザーのシナリオをサポートします。 複数のチーム メンバーが同時に Go-live レビューに関する詳細を提供できます。
- Go-live 準備完了レビューのすべての質問への回答が完了したら、**送信** を選択して Microsoft にレビューを提出します。

### <a name="after-the-review-is-submitted-in-the-portal"></a>ポータルでレビューが提出された後

- Microsoft FastTrack は、プロジェクトをレビューし、潜在的なリスク、ベスト プラクティス、プロジェクトの Go-Live を成功させるための推奨事項を説明するレポートを提供します。 **レビューでは、初期レポートに最大 3 営業日、さらにリスク軽減が必要な場合は追加で時間を要する場合があります。**
- ポータルの **レビュー参加者** として選択されたユーザーは、レビューに関する更新を提供する電子メール通信を受信します。
- すべての重要なリスクへの対処が完了し、レビューが完了すると、Microsoft により LCS プロジェクトの運用環境スロットが有効になります。 次に顧客/パートナーは運用環境の配置をトリガーします。

> [!NOTE]
> ポータルに問題が発生した場合は、ポータル右上隅で **お問い合わせ** を選択するか、<ftd365ip-support@microsoft.com> まで電子メールを送信してポータル サポート チームにご連絡ください。 電子メールには、LCS のプロジェクトの ID を指定し、問題を説明する詳細を記述してください。

## <a name="production-environment-deployment"></a>運用環境を配置する

> [!NOTE]
> 運用環境は、業務運営を実行するためにのみ使用する必要があります。 テスト、デモ、またはトレーニング目的では使用できません。 切替、および切替モック (切替モックを計画した場合) を運用で実行できます。 ソリューションをテストするには、テストに必要なすべての要素とサービスが含まれる適切なサンドボックス環境を使用します。

環境を配置するには、サービス アカウントを選択することをお勧めします。 たとえば、配置する環境の管理者ユーザーとして、汎用ユーザー アカウントを選択します。 名前付きユーザー アカウントを選択すると、そのユーザーが使用できない場合は、環境にアクセスすることができない場合があります。 管理者ユーザーが環境にアクセスする必要があるいくつかのシナリオ例を次に示します:

- **最初の配置後の任意の環境への最初のサインイン** – 管理者ユーザーだけが環境にアクセスできます。
- **運用環境からデータベースをリフレッシュした後のサンドボックス環境への最初のサインイン** – 管理者アカウント以外のユーザー アカウントはサインインできません。

運用環境は、サンドボックス環境が配置され、UAT とパフォーマンス テストが行われたのと同じデータセンターに配置される必要があります。 ネットワーク要件および待機時間テストの実行方法については、[ネットワーク要件](../get-started/system-requirements.md#network-requirements)を参照してください。

運用配置には約 30 分かかります。 配置が完了すると、電子メール通知が環境管理者に送信されます。

運用環境は、LCS プロジェクトに割り当てられたライセンス数、および[サブスクリプション見積もりツール](../../dev-itpro/lifecycle-services/subscription-estimator.md)のトランザクション量に基づいてサイズ決定されます。

生産が配置された後、プロジェクト チームは、[運用環境への更新の導入](../../dev-itpro/deployment/updateenvironment-newinfrastructure.md#promote-an-update-to-production-environments)の指示に従って配置可能パッケージを適用し、データを移行できます。 データ移行に関しては、非運用環境でデータの準備と検証してから、[サンドボックス データベースを運用環境にコピーする](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md#copy-the-sandbox-database-to-production)ことをお勧めします。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


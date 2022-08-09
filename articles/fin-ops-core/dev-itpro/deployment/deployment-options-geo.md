---
title: ローカル地域における Dynamics 365 Finance、Supply Chain Management、および Commerce
description: この記事では、サポートされた Microsoft Dynamics 365 Commerce、Dynamics 365 Finance、および Dynamics 365 Supply Chain Management の地域とエンドポイントに関する情報を提供します。
author: Shailesh4all
ms.date: 04/28/2022
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2022-04-28
ms.openlocfilehash: 73fd2af074f6e554451714f844f5ee71e24c66a1
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103538"
---
# <a name="dynamics-365-finance-supply-chain-management-and-commerce-in-local-geographies"></a>ローカル地域における Dynamics 365 Finance、Supply Chain Management、および Commerce

[!include[banner](../includes/banner.md)]

## <a name="data-residency"></a>データ所在地

Microsoft Dynamics 365 Commerce、Dynamics 365 Finance、および Dynamics 365 Supply Chain Management は、一般的に特定の地域でのデータ所在地をサポートするため利用可能です。 配置オプションでは、ローカルのデータ所在地を必要とする特定地域のエンティティとビジネスを行う規制対象の業界、または商業組織の顧客にサービスを提供します。

すべての必要なサービスおよび関連データは、地域の対応するデータ センターに配置されます。 これらのサービスとデータには、Microsoft Dynamics Lifecycle Services (LCS)、利用統計情報、データベース、および環境が含まれます。 顧客データは地理的境界から離れません。

### <a name="supported-local-geographies-and-endpoints"></a>サポートされるローカルの地域とエンドポイント

次の表に、Commerce、Finance、および Supply Chain Management でサポートしているローカル地域とエンドポイントの一覧を示します。

| 場所 | LCS エンドポイント |
|-----------|--------------|
| フランス | [https://fr.lcs.dynamics.com/](https://fr.lcs.dynamics.com/) |
| アラブ首長国連邦 | [https://uae.lcs.dynamics.com/](https://uae.lcs.dynamics.com/) |
| 南アフリカ | [https://sa.lcs.dynamics.com/](https://sa.lcs.dynamics.com/) |
| スイス | [https://ch.lcs.dynamics.com/](https://ch.lcs.dynamics.com/) |
| ヨーロッパ | [https://eu.lcs.dynamics.com/](https://eu.lcs.dynamics.com/) |
| ノルウェー | [https://no.lcs.dynamics.com/](https://no.lcs.dynamics.com/) |

## <a name="feature-availability-in-local-geographies"></a>ローカル地域の利用可能な機能

Microsoft は、地域をまたがって業務上使用できるサービス間で同等の機能を維持しています。 例外は次の一覧に示されています。 この一覧は、ビジネス アプリケーション ソリューションの実装が成功することを理解および計画するのに役立ちます。

これらのサービスおよび機能を今後のリリースに含めること、および更新の対象として引き続き評価します。

- Dynamics Regulatory Alert Submission サービスは、単一のグローバル サービスとして機能するので、ローカル地域では使用できません。 ただし、 Global LCS からサービスにアクセスできます。
- 会社のライブラリは、American Productivity & Quality Center (APQC) ビジネス プロセス モデラー (BPM) ライブラリで利用可能です。 各ローカル地域のために、LCS は概要ライブラリと最後に公開された APQC ライブラリのみを公開します。 ライブラリをプロジェクト ライブラリにコピーして、法人ライブラリとして編集および公開できます。
- Dynamics 365 Translation Service は、アメリカ合衆国および欧州連合 (EU) でのみ使用できます。
- 電子レポート (ER) 資産は、共有資産ライブラリに表示されません。 ただし、LCS Global 資産ライブラリから手動でアップロードできます。 この問題を回避するには、Microsoft エンジニアリングによって提供されるスクリプトを実行します。 または、Global リポジトリに接続して Microsoft Support ER 資産にアクセスすることもできます。 詳細については、 [Regulatory Configuration Service (RCS) - Lifecycle Services (LCS) ストレージの廃止](../../../finance/localizations/rcs-lcs-repo-dep-faq.md) を参照してください。
- 埋め込み型の Power BI ダッシュボードは使用できません。
- LCS の環境監視では、Global LCS と同じダッシュボード インターフェイスは公開されません。 ただし、コア キー パフォーマンスのインジケーターは利用可能です。
- ホストされているエージェントを使用する Azure ビルド パイプラインの場合、LCS ライブラリからのナゲット パッケージは共有資産ライブラリで使用できません。
- コマースおよび E コマースの Cloud スケール ユニットは、アメリカ合衆国およびヨーロッパでのみ使用できます。
- 計画の最適化サービスは利用できません。
- ローカル ビジネス データの配置は、ヨーロッパでのみ使用できます。
- Dynamics AX 2012 から財務と運用アプリに更新するコード アップグレード機能は、LCS 米国 (lcs.dynamics.com) 以外の地域では使用できません。

例外の詳細や地域サービスに関する質問については、[Microsoft Dynamics 365 サポート](https://dynamics.microsoft.com/support/) に問い合わせください。

国およびワークロードごとの製品の可用性については、[Dynamics 365 および Power Platform の可用性](https://dynamics.microsoft.com/availability-reports/) を参照してください。


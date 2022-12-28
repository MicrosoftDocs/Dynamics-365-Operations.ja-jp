---
title: Operational Insights の設定
description: この記事では、Microsoft Dynamics 365 Commerce で Operational Insights 機能を設定し使用する方法について説明します。
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832128"
---
# <a name="set-up-operational-insights"></a>Operational Insights の設定

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で Operational Insights 機能を設定し使用する方法について説明します。

Operational Insights は、顧客が所有する Application Insights アカウントにテレメトリを直接送ることで、サービスの正常性と業務機能を顧客に深く把握するために設計された Dynamics 365 Commerce 機能です。

Commerce Headquarters で環境に対して Operational Insights を有効にすることで、Commerce Scale Unit (CSU) と販売時点管理 (POS) デバイスの両方から、イベントの集金リストを収集できます。 これらのイベントを利用すると、システムの実行状況を理解し、技術的および業務上の重要なメトリクスを監視することができます。

この機能の機能を使うのが好きな場合は、特定の環境でコレクションをすばやく有効または無効にすることで便利です。 これにより、開発時または生産時のトラブルシューティングやデバッグに役立ちます。

## <a name="access-logs-in-application-insights"></a>Application Insights のログへのアクセス

Application Insights を介して Commerce CSU コンポーネントおよび POS コンポーネントの診断イベント ログにアクセスするには 、このセクションの手順を実行します。

### <a name="minimum-version-requirements-for-csu"></a>CSU の最小バージョン要件

CSU には、次の最小バージョン要件があります。

- 10.0.23 (Retail Server バージョン 9.33.22062.15 およびそれ以降)
- 10.0.24 (Retail Server バージョン 9.34.22062.14 およびそれ以降)
- 10.0.25 (Retail Server バージョン 9.35.22062.13 およびそれ以降)
- 10.0.26 およびそれ以降 (すべてのバージョン)

### <a name="enable-diagnostic-events-in-application-insights"></a>Application Insights の診断イベントを有効にする

> [!IMPORTANT]
> システム オペレーション インサイト プレビューを使用した場合、次の手順を実行してシステム オペレーション インサイトを有効にする必要があります。 このようにして、イベントに対し信頼性があり安全なアクセスを継続することができます。

Commerce コンポーネントの診断イベントを有効にするには、Application Insights アカウントが必要です。 既存のアカウントを使用するか、または[新しいアカウントを作成](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource)できます。 データ プライバシーの理由から、運用、サンドボックス、および開発環境とで個別の Application Insights アカウントを使用することをお勧めします。 アカウントを作成した後、headquarters で **Operational Insights** 機能を有効にする必要があります。

Application Insights で診断イベントを有効にするには、次の手順に従います。

1. headquarters で、**機能管理** ワークスペースを開いて、**Operational Insights** 機能を有効にします。
1. **システム管理 \> 設定 \> オペレーション情報分析** に移動します。
1. **構成** タブで、**Commerce チャネル イベント** オプション を **はい** に設定します。
1. **環境** タブで、Application Insights を使用する計画があるすべての環境に対して **LCS 環境 ID** と **環境モード** の値を入力します。 各環境の LCS 環境 ID は、Microsoft Dynamics Lifecycle Services の環境の **環境の詳細** ページで見つけることができます。 データベースのコピー操作が実行されるときに診断イベントが正しくない環境に誤って送信されるのを防ぐために、この手順が必要です。
1. **Application Insights レジストリ** タブで、各 Application Insights アカウントを使用する環境の Application Insights **インストルメンテーション キー** の値および対応する **環境モード** の値を指定します。
1. 前の構成が完了した後、**CDX Job 1110** ジョブを実行する必要があります。 このジョブが独自のスケジュールで実行されるのを待つか、手動で実行することができます。
1. Lifecycle Services で、**環境の詳細 \> Commerce \> 管理** に移動して、CSU インスタンスを選択して **再起動** を選択します。 各 CSU について、このステップを繰り返します。
1. Application Insights を使用にする環境ごとに前の手順を繰り返します。

> [!NOTE]
> - Operational Insights 内のテレメトリ イベントは変更される可能性があります。 Operational Insights イベントを使用して、予備分析やトラブルシューティングを自分でおこない、ダッシュボードや警告を定義しないことをお勧めします。 セルフサービスのトラブルシューティング以上の目的でイベントを使用する場合は、各 CSU/POS のリリース後にクエリを検証および更新することをお勧めします。
> - Commerce バージョン 10.0.29 では、このセクションの手順により、POS Operational Insights のストリーミングを Application Insights アカウントに対して有効にすることもできます。 詳細については、[POS 用 Operational Insights - イベントとクエリ](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf) を参照してください。

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>DLLHost.exe. 構成ファイルを使用して POS Operational Insights を制御する

DLLHost.exe. 構成ファイルを使用して POS Operational Insights を制御するには、これらの手順に従います。

1. テキスト エディターで、**C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker** にある **DLLHost.exe.config** ファイルを開きます。
1. **diagnosticsSection** セクションで、クラス名 **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsights.OperationalInsightsLogger** を持つシンク XML 要素を削除します。
1. ファイル保存します。

### <a name="disable-diagnostic-events-in-application-insights"></a>Application Insights の診断イベントを無効にする

> [!IMPORTANT]
> 診断イベントを無効化して、それらを Application Insights へ送信しないようにするには、次の手順を完了させる必要があります。 機能管理で、この機能を無効化することはできません。

Application Insights で診断イベントを無効化にするには、次の手順に従います。

1. headquarters で、**システム管理 \> Operational Insights** に移動します。
1. **構成** タブで、**Commerce チャネル イベント** オプション を **いいえ** に設定します。
1. 前の構成が完了した後、**CDX Job 1110** ジョブを実行する必要があります。 このジョブが独自のスケジュールで実行されるのを待つか、手動でジョブを実行することができます。
1. Lifecycle Services で、**環境の詳細 \> Commerce \> 管理** に移動して、CSU インスタンスを選択して **再起動** を選択します。 各 CSU について、このステップを繰り返します。
1. Application Insights を無効にする環境ごとに前の手順を繰り返します。

単一の環境に対して診断イベントを無効にするには、**オペレーション インサイト** ページの **Application Insights レジストリ** タブにあるインストルメンテーション キーを削除します。 前の手順の手順 3 と 4 を実行します。

> [!NOTE]
> Commerce バージョン 10.0.29 以降では、このセクションのステップにより、POS Operational Insights のイベントのストリーミングを Application Insights アカウントに対して無効化することもできます。 

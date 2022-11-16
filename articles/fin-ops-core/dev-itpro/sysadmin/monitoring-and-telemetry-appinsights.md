---
title: Application Insights による監視と利用統計情報
description: この記事では、財務と運用アプリ向け Application Insights の統合を使用、設定、構成する方法について説明します。
author: LaneSwenka
ms.date: 10/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: twheeloc
ms.custom: 257614
ms.assetid: 558598db-937e-4bfe-80c7-a861be021db1
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-09-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba63c5b53de3464ef44b94d9159fa86cbdf2c95
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748916"
---
# <a name="monitoring-and-telemetry-using-application-insights"></a>Application Insights による監視と利用統計情報

財務と運用アプリの監視と利用統計情報機能は、財務および運用アプリのインスタンスとターゲットの Application Insights 送信先との間の直接的なポイント ツー ポイント統合です。 この機能を使用すると、開発者や管理者はアプリケーションの問題をほぼリアルタイムでトリアージし、解決できます。  生成された利用統計情報は、サポートや他の運用レポートのために Microsoft によって収集されることはありません。 代わりに、データは顧客が所有し、顧客主導です。

## <a name="what-telemetry-is-entered-in-application-insights-and-in-which-tables"></a>どの利用統計情報が Application Insights に入力され、どのテーブルに入力されますか?

次の表では、X++ から取得される様々な利用統計情報の種類と、Application Insights のターゲット テーブル名について説明します。

| 利用統計情報タイプ | Application Insights のテーブル名 |
|----------------|------------------------------------|
| FormRun フォームの読み込み | pageViews |
| X++ 例外 | 例外 |
| X++ カスタム イベント | customEvents |
| X++ カスタム メトリックス | customMetrics |

Application Insights には、このデータの使用に役立つさまざまな機能があります:

- 組織の正常性の概要に関する [ダッシュボードを作成](/azure/azure-monitor/visualize/tutorial-logs-dashboards) します。
- [スマート検出](/azure/azure-monitor/app/proactive-diagnostics) を使用してプロアクティブ監視を実行します。
- 組織に基づいて重要なシナリオに関する [警告を設定](/azure/azure-monitor/app/tutorial-alert) します。
- 一般的な [ナビゲーション パターンを使用の観点から](/azure/azure-monitor/app/usage-flows) 視覚化および追跡します。 たとえば、ユーザーはメイン タブに戻ってページを閉じる前に、常に特定のタブを選択します。 このパターンは、ユーザーの時間を節約するために、最初のタブにフィールドを配置することを示している場合があります。
- 左ウィンドウの **監視** でアクセスできる [ログ](/azure/azure-monitor/log-query/log-query-overview) パネルを使用して、パフォーマンスとエラーのトラブルシューティングを行うカスタム クエリを作成します。

## <a name="overview-panel-in-application-insights"></a>Application Insights の 概要パネル

Application Insights では、収集された利用統計情報データの異なるビューが提供されます。 **トランザクション検索** パネルには、財務と運用アプリからさまざまな診断およびイベントの詳細な一覧が表示され、ポータルのその他の機能へのゲートウェイとなります。 詳細については、各エントリを掘り下げて確認できます。 次の図は、例を示します。

[![Application Insights 概要。](./media/AppInsights/overview.png)](./media/AppInsights/overview.png)

一覧をフィルター処理して、必要な利用統計情報の種類のみを表示できます。 結果のビューは、Azure ダッシュボードに保存できます。
 
## <a name="performance-panel-in-application-insights"></a>Application Insights のパフォーマンス パネル

**パフォーマンス** パネル は、現在この機能で使用されていませんが、将来使用される可能性があります。

## <a name="failures-panel-in-application-insights"></a>Application Insights のエラー パネル

**エラー** パネルを開くには、左ウィンドウで **調査中のエラー** を選択するか、**失敗した要求** グラフを選択します。
 
**エラー** パネル の情報は、Application Insights の例外テーブルから取得されます。 X++ で取得される例外はすべて、**System.Exception** タイプの 一般例外として表示されます。 パネルには、失敗した要求の数と、アプリケーションの各操作で影響を受けたユーザーの数が表示されます。 操作を選択して、エラーの詳細を表示できます。 標準のビジネス ロジック、X++ のカスタマイズ、独立したソフトウェア ベンダー (ISV) ソリューションに関連するエラーが、ここでキャプチャされます。 これらのエラーには、ブラウザーの対話型ユーザー活動によって生成されるエラーと、バッチ Application Object Server (AOS) インスタンスでデータを非同期処理するバッチ ジョブが含まれます。 操作を選択すると、操作に関する詳細情報が右ウィンドウに表示されます。
 
利用統計情報プロパティでは、エラーが **対話型** または **バッチ** の実行モードで発生したかどうか、どのユーザーから発生したか、どの法人から発生したかを判断できます。 例外は、Application Insights から標準的な統合を使用して、Microsoft Azure DevOps または GitHub のバグとして記録できます。 また、選択したバグ追跡システムでバグを記録することもできます。

[![Application Insights 例外。](./media/AppInsights/Exceptions.png)](./media/AppInsights/Exceptions.png)

詳細については、[Azure Application Insights を使用した実行時例外の検索および診断](/azure/azure-monitor/learn/tutorial-runtime-exceptions) を参照してください。

## <a name="querying-data-in-application-insights"></a>Application Insights でのデータのクエリ

Application Insights の左ウィンドウにある **監視** の下で、**ログ** を選択して **ログ** パネルを開きます。
 
### <a name="common-fields"></a>共通フィールド

Application Insights に入力されるすべての利用統計情報とイベントには、次のフィールドにがあります:

- **cloud\_RoleInstance** – このフィールドは、インスタンス タイプ (サンドボックスおよび運用の配置用の **ServiceFabric**、または仮想マシン (VM) ベースの配置用のクラウド ホスト環境名など) に設定されます。
- **session\_Id** – このフィールドでは、1 つのユーザー セッション内のすべての活動を一意に識別します。 セッション ID は、ユーザーが新しいタブを開いたり、**F5** キーまたは **更新** ボタンを選択したり、アプリを終了して再度開いたりしたときにリセットされます。

    > [!NOTE] 
    > このフィールドは、**ユーザー セッション** の利用統計情報が構成されている場合にのみ有効になります。

 - **user\_Id** – このフィールドは、現在、財務と運用アプリの UserInfo テーブルからユーザー ID に設定されています。 
 
    > [!NOTE] 
    > このフィールドは、**ユーザー セッション** の利用統計情報が構成されている場合にのみ有効になります。

- **client\_IP** – Application Insights は、一般データ保護規則 (GDPR) に準拠するために、このフィールドを常に **0.0.0.0** に設定します。 提供されるインターネット プロトコル (IP) アドレスは、**client\_City**、**client\_StateOrProvince**、**client\_CountryOrRegion** フィールドを設定するために使用されます。
- **message** – このフィールドは、ユーザーに表示されるユーザーのローカル言語でのエラー メッセージ、およびエラー タイプの利用統計情報でエラーが発生した X++ スタック トレースを取得するために使用します。
- **カスタム プロパティ - LegalEntity** – このフィールドは、利用統計情報が発生した法人コードに設定されます。
- **カスタム プロパティ - BatchJobId** – このフィールドは、利用統計情報で結果となったバッチ ジョブのレコード ID に設定されます。
- **カスタム プロパティ – ExecutionMode** – このフィールドは、ブラウザーによって開始される利用統計情報に対しては **対話型** に、バッチ ジョブに対しては **バッチ** に設定されます。 **バッチ** に設定されている場合は、付随する **BatchJobId** 値が入力されます。

## <a name="enable-the-public-preview-feature"></a>パブリック プレビュー機能の有効化

> [!NOTE]
> この機能は、現在、Azure China または Azure Government で使用できません。 利用できる状態になったら、一般公開されている機能に追加するように取り組んでいきます。 現在、すべての利用統計情報は、Azure パブリック クラウドにのみ送信されます。 したがって、現時点では、Azure China または Azure Government のインストルメンテーション キーを指定することはできません。

この機能はパブリック プレビュー段階です。 有効にするには、**機能管理** ワークスペースを開き、**監視と利用統計情報** 機能を有効にします。 その機能が表示されず、プライベート プレビュー機能が有効になっている場合は、まずプライベート プレビューを無効にする必要があります。 詳細については、この記事の次のセクションを参照してください。

機能を有効にした後、パラメーターを構成する必要があります。

1. **システム管理 \> 設定 \> 監視と利用統計情報パラメーター** の順に移動します。
2. **環境** タブで、各環境に Microsoft Dynamics Lifecycle Services 環境 ID を入力し、環境を **開発**、**テスト**、または **運用** 環境として分類します。 環境 ID は、Lifecycle Services の **環境の詳細** ページから取得できます。
3. **Application Insights レジストリ** タブで、特定の Application Insights 送信先に利用統計情報を送信する環境のカテゴリを指定します。 たとえば、開発者の利用統計情報はある場所に移動でき、、運用の利用統計情報は別の場所に移動できます。
4. 上部の **構成** タブで、取得する利用統計情報の各タイプをオンにし、取得しない各タイプをオフにできます。 すべてのタイプをオンのままにすることも、問題を診断する必要がある場合にのみ有効にすることもできます。 

> [!NOTE]
> 利用統計情報が無効になった後、キャッシュがあるため数分間は送信を停止しません。 また、利用統計情報を無効にすると、Application Insights で有効にしている場合でも、プロアクティブ警告を受け取ることができません。 利用統計情報を有効にすると、Application Insights で使用と潜在的な追加費用が発生します。

## <a name="disable-the-private-preview-feature"></a>プライベート プレビュー機能の無効化

プライベート プレビュー ソフトウェアがインストールされている場合は、Lifecycle Services を使用して環境から削除する必要があります。 このプロセスを [パッケージのアンインストール](/dynamics365/fin-ops-core/dev-itpro/deployment/uninstall-deployable-package) の手順に従って、定期的にスケジュールされた次のパッケージ配置にバンドルすることができます。

プライベート プレビューを削除すると、**機能管理** ワークスペースの **監視と利用統計情報** 機能が表示されます。 パブリック プレビューではスキーマ名が同じなので、この機能を有効にした場合、プライベート プレビューからの設定や構成は変更されません。 したがって、プライベート プレビュー バージョンを削除してもデータは失われません。

[!include [banner](../includes/banner.md)]

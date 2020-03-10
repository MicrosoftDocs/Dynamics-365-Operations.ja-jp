---
title: 1 つのバージョンのサービス更新に関するよく寄せられる質問
description: このトピックは、一貫性があり、予測可能でシームレスな方法で最新の状態に保つために使用できるサービスの更新、プロセス、ツールを明確にすることを目的としています。
author: ShellyBakke
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: smiller
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4ce09fc234d8ba3aa195ab2a375db0ec5500b562
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2020
ms.locfileid: "3058002"
---
# <a name="one-version-service-updates-faq"></a>1 つのバージョンのサービス更新に関するよく寄せられる質問

[!include[banner](../includes/banner.md)]

2018 年 7 月、一貫性があり、予測可能でシームレスな方法で最新の状態に保つのに役立つ [Dynamics 365 の更新の提供方法の変更](https://cloudblogs.microsoft.com/dynamics365/2018/07/06/modernizing-the-way-we-update-dynamics-365/)を発表しました。  2019 年 6 月、顧客からのフィードバックに基づき、[利用可能な新しい柔軟なサービスの更新](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/06/03/new-flexible-service-updates-for-dynamics-365-for-finance-and-operations/)を発表しました。 このよく寄せられる質問は、準備のために使用できるサービスの更新プログラム、プロセス、ツールを明確にすることを目的としています。 必要に応じて、このトピックに追加情報を追加し続けします。


### <a name="can-the-update-be-delayed-what-is-the-policy"></a>更新を遅らせることができますか、ポリシーとは何ですか。
はい、Lifecycle Services プロジェクトの更新の設定を使用して、更新の一時停止、遅延、またはオプトアウトを行うことができます。  顧客は、最大 3 つまでの更新を続けて一時停止することができます。 以下は、遅延更新の例です。 
- 顧客は現在バージョン 10.0.2 を使用しています。
- 顧客は、更新 10.0.3、10.0.4、および 10.0.5 を一時停止できます。
- 顧客は、10.0.6 更新が利用可能になったら、それを入手する必要があります。
  
### <a name="with-a-release-date-in-early-april-when-will-the-general-availability-package-be-made-available"></a>4月の始めのリリースで、一般提供パッケージはいつ使用可能になりますか。
月次リリースの製品更新プログラムは、月の 1、2、3 週間目に予定されています。 Lifecycle Services (LCS) でセットアップした構成により、その特定の週に更新プログラムを受け取ります。
 
4 月 10.0 リリースの場合、Microsoft は LCS でセットアップした構成に基づいて 4 月 6 日、4 月 13 日、または 4 月 20 日の週末に更新プログラムを実行します。 サンドボックスの更新プログラムは、常にその更新の 1 週間前にスケジュールされます。 コンフィギュレーション設定は LCS で利用できます。

ユーザーは、Lifecycle Services で提示されているよりも早い時期、またはより都合のいい時間に更新プログラムを適用することを選択できます。  顧客が最新バージョンを使用している場合、自動更新がキャンセルされます。  

## <a name="service-updates"></a>サービスの更新

### <a name="what-product-versions-are-impacted-by-service-updates"></a>どの製品バージョンがサービスの更新プログラムの影響を受けますか?

| バージョン       | 説明 |
|---------------|-------------|
| 8.1 以降 | 8.1 以降のすべてのユーザーは、2018 年 11 月以降アプリケーションとプラットフォーム更新が結合された毎月の自動更新プログラムがスケジュールされています。 4 か月以内または 3 つのサービス更新プログラム以内に更新する必要があります。 更新を一時停止するには、[サービスの更新の一時停止](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/pause-service-updates)を参照してください。 |
| 8.0           | 8.0 をご利用のユーザーは、毎月のプラットフォーム更新プログラム と財務報告の更新をマニュアルで適用することが可能です。 4 か月または 3 つのサービス更新以内に更新する必要があります。 2019 年 4 月で 8.0 アプリケーションのライフサイクルが終了します。 8.0 を使用している顧客は、サポートを維持するには 2019 年 4 月 30 日までに更新する必要があります。 アプリケーションのサポート対象となるには、手順にに従って最新バージョンに更新する必要があります。 詳細については、 [バージョン 8.0 から 10.0.X への環境の更新](../../dev-itpro/migration-upgrade/appupdate-80-81.md)を参照してください。 | 
| 7.x           | 7.x をご利用のユーザーは、毎月のプラットフォーム更新プログラム と財務報告の更新をマニュアルで適用することが可能です。 4 か月以内の更新プログラムと 3 つのサービス更新が必要です。 7.x をご利用の顧客は、2019 年 4 月 30 日までに更新をしない場合はサポートが失効します。 2019 年 4 月 30 日以降もバージョン7.3 の顧客には、毎月自動プラットフォーム更新プログラムが送信されます。 2019 年 4 月中までに8.1にアップグレードする必要があります (拡張機能を使用できない場合は除きます)。 市販されているオーバーレイ済のバージョンは7.3です。 

### <a name="what-does-the-service-update-contain"></a>サービス更新プログラムには何が含まれていますか?

リリース 8.1 以降では、サービスの更新には、規制の更新を含むサービスの重要な改良であるアプリケーション (財務、レポート、コマースを含む) とプラットフォームの変更が含められます。 新しいエクスペリエンスは構成可能になります。 サービス更新プログラムには、下位互換性があります。 この更新プログラムを代表する 1 つのバージョンがあります。

### <a name="what-is-a-regulatory-update"></a>規制の更新とは何ですか?

規制の更新は、法律 (通常は特定の国/地域) によって義務付けられている新機能または既存の機能の変更です。 規制の更新は、特定の法律実施日 (LED) に常に要求され、この日付以前に有効にする必要があります。

### <a name="whats-the-upcoming-schedule-of-updates"></a>更新の将来のスケジュールとは何ですか?

サービスの更新は、2018 年 11 月から提供されています。 都合の良いときに更新プログラムを適用したり、選択された保守時間帯に基づいてマイクロソフトがサービス更新を自動適用するようにしたりするオプションがあります。 4 か月以内に更新する必要があります。

対象となるリリースのスケジュールについては、 [サービス更新の可用性](public-preview-releases.md)を参照してください。

### <a name="are-there-any-major-updates-post-81"></a>8.1 以降のメジャー アップデートはありますか?

4 月と 10 月に、新しいエクスペリエンスを有効にする 2 つのメジャー アップデートがあります。 メジャー アップデートは、コードやデータのアップグレードは必要ありません。 重大な変更は、お客様が計画できるように、12 か月前にお知らせします。 このような変更は、メジャー アップグレード時にのみ導入されます。 2019 年 4 月に利用可能になる 10.0 リリースも、アップグレードではなく更新プログラムになります。

### <a name="what-does-it-mean-when-an-update-is-backward-compatible"></a>更新プログラムに下位互換性がある場合、これは何を意味しますか?

下位互換性では、バイナリと機能の互換性がカバーされます。 バイナリ互換性は、カスタマイズを再コンパイル、再設定、または再展開しなくても、あらゆるランタイム環境に更新プログラムを適用できることを意味します。 また、デザイン時の開発環境で、X++ パブリックおよび保護された API とメタデータが変更または削除されないことも意味します。 Microsoft が古い形式の API を削除することによって互換性をなくす必要がある場合、廃止スケジュールが 12 か月前に発表されます。 機能互換性は、ユーザー エクスペリエンスに関するもので、すべての新しいエクスペリエンスは 12 か月間オプトインになります。

下位互換性には、非 X++/メタデータ API は含まれていません。 Microsoft は、事前に通知することなく、製品が使用する依存関係を更新し、依存関係を削除する権限を保有します。 Microsoftは、明記された場合を除いて、依存ソフトウェア ライブラリの下位互換性を維持することを約束しません。 

非推奨のガイドライン、非推奨のメソッドおよびメタデータ要素の詳細については、[メソッドとメタデータの要素の非推奨](../../dev-itpro/migration-upgrade/deprecation-deletion-apis.md) を参照してください。

### <a name="can-i-apply-a-platform-service-update-to-my-existing-81-or-later-environments"></a>プラットフォーム サービスの更新を既存の 8.1 以降の環境に適用することができますか。

8.1 以降の顧客は、8.1.x または v10.x のサービス更新プログラムのみ適用することができます。 プラットフォームのみのサービスの更新をバージョン 8.1 以降に適用することはできません。 プラットフォームのサービスの更新はバージョン 7.x または 8.0 にのみ適用できます。

### <a name="will-platform-updates-be-able-to-be-scheduled-and-delaypause-by-customers"></a>プラットフォームの更新をユーザーがスケジュール設定して遅らせたり一時停止させることはできますか。

はい、バージョン 7.3 を使用している顧客は、Lifecycle Services で直接プラットフォーム更新プログラムをスケジュールできるようになります。 遅延/一時停止 エクスペリエンスも利用可能になります。

### <a name="do-these-updates-apply-to-on-premises"></a>これらの更新プログラムはオンプレミスで適用されますか?

使用しているバージョンの具体的な有効期限については、[ソフトウェアのライフサイクル ポリシーおよびオンプレミス リリース](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/on-prem-version-update-policy?toc=/fin-and-ops/toc.json)を参照してください。 一般に 3 つのサービス更新の有効期限があります。 ただし、このトピックで説明されている更新のプロセスは、クラウド サービスにのみ適用されます。

## <a name="process"></a>処理

### <a name="how-will-microsoft-ensure-quality-of-releases"></a>Microsoft はリリースの品質を確保していますか?

リリースの品質を保つことは基本的な原則であり、 [サービス更新の可用性](public-preview-releases.md) で説明されている一連の進歩的かつ厳格な自動検証によって可能になっています。

### <a name="can-i-select-the-day-and-time-to-update"></a>更新する日時は選択できますか?

ユーザーは、LCS に日と保守の時間枠を構成できます。 更新方法に含まれる手順をが記載された LCS 通知を受信するように選択したユーザーには、メールが送信されます。 ユーザーは、更新プログラムの指定された階層 2/UAT サンドボックスを選択できるようになります。 ユーザーは、テストと検証に 7 カレンダー日かけることができます。 お客様は、LCS からのすべての環境に対して、以前の更新を適用することもできます。 実稼働準備ができた配置可能パッケージは、Lifecycle services のアクション センターからすべての顧客が入手できます。 ユーザーには、更新を追加サンドボックスまたは開発者/ビルド (階層 1) 環境に展開する責任があります。

### <a name="a-service-update-was-applied-to-the-environment-when-looking-at-the-tile-in-lifecycle-services-for-this-environment-what-does-the-number-on-the-tile-represent"></a>サービスの更新が環境に適用されたて、この環境の Lifecycle Services のタイルを見たとき、タイルの番号に表示される数字は何を表しますか。

同じサービス更新が、Microsoft によってすべての顧客に自動適用されます。 Microsoft は、引き続き最新の更新プログラムを提供します。 その環境の LCS のタイルは、環境に適用できる修正プログラム数の累計を表します。 Microsoft は、すべての顧客に同じバージョンのみ自動適用するため、必要な場合、お客様には累積的な修正プログラム パッケージを適用する責任があります。

### <a name="how-do-i-update-to-the-latest-version"></a>最新バージョンに更新する方法を教えてください。

ユーザーは、LCS の環境の詳細ページでタイルを使用して最新バージョンに更新できます。 Microsoft により更新プログラムがリリースされたら、タイルに利用可能な更新プログラムが表示されます。 ユーザーは、サンドボックスと製造環境で更新エクスペリエンスを経由して独自に更新プログラムを適用することができます。 

### <a name="how-do-i-update-the-production-environment-to-the-same-version-after-microsoft-updates-the-sandbox-environment"></a>Microsoft がサンドボックス環境を更新した後で、実稼働環境を同じバージョンに更新する方法を教えてください。

Microsoft がサンドボックス環境を更新すると、更新に使用されるパッケージはプロジェクトの資産ライブラリに保存されます。 パッケージ名の先頭には "サービスの更新" という語が付いています。 そのパッケージはすでにサンドボックス環境に適用済みのため、このパッケージをリリース候補としてマークできます。 その後で実稼働環境に移動し、他の更新プログラムを適用するのと同様にパッケージを適用するようスケジュールすることができます。

### <a name="what-is-the-expected-downtime"></a>予想されるダウンタイムはどのくらいですか ?

更新が正常に完了するために予想されるダウンタイムは 1 時間 30 分です。 ただし、 更新プログラムの適用時に問題が発生する場合、3 時間のダウンタイムを要求します。 マイクロソフトは、必要とするダウンタイムを減らすために積極的に取り組んでいます。改善は数か月以内に反映されます。

### <a name="whats-the-process-for-deprecation"></a>廃止のプロセスを教えてください。

[Finance and Operations 削除済または非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックで、削除済の機能と非推奨の機能の違いを次のように述べます。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

### <a name="can-i-delay-an-update"></a>更新プログラムを延期することはできますか?

LCS コンフィギュレーションを介して最大 4 か月または連続する 3 つのサービス更新プログラムの更新を延期できます。 この期間後は、更新プログラムがスケジュールされ、Microsoft により自動適用されます。 遅延更新用の更新エクスペリエンスにより、さらなるダウンタイムが発生します。

### <a name="can-i-delay-an-update-for-longer-than-3-consecutive-service-updates-due-to-seasonal-activity-or-other-business-reason"></a>季節的なアクティビティやその他のビジネス上の理由により、3 つの連続したサービス更新よりも長く更新を遅らせることはできますか? 

いいえ、サービス更新はサンドボックスに自動的に適用されます。 そして7 日後、環境が 3 サービス更新より古い場合、更新が実稼働環境に適用されます。 顧客は、最大 3 つの連続した更新のみ連続して一時停止できます。 たとえば、バージョン 10.0 の顧客が 10.0.1、10.0.2、および 10.0.3 の更新を一時停止する場合、サービスの更新プログラム 10.0.4 はサンドボックスに自動適用されます。 

### <a name="what-if-i-find-an-issue-during-the-sandbox-update"></a>サンドボックスの更新中に問題が発生した場合はどうなりますか?

サンドボックス環境で検証を行うときに問題が見つかった場合は、有効なサポート チケット番号と業務の妥当性を提供することで直接 LCS を通じて更新をスキップするように要求できます。 

### <a name="what-if-i-find-a-critical-issue-during-sandbox-testing-and-i-am-not-able-to-pause-the-production-auto-update"></a>サンド ボックスのテスト中に重大な問題が見つかり、実稼働環境の自動更新プログラムを一時停止できない場合はどうなりますか。

識別されたらすぐに、重要な問題は常に Lifecycle Services 経由でサポート チームに送信される必要があります。 サポート スタッフは、重要な問題に対する解決策を扱います。

### <a name="how-much-time-do-i-get-for-validation"></a>検証にかけることができる時間はどのぐらいですか?

更新がサンドボックス環境に適用されてから、7 暦日間検証できます。 もっと多くの時間が必要な場合、Lifecycle Service のアクション センターを使用して配置可能なパッケージにアクセスし、環境に適用できます。 これで、生産ロールアウトよりも前に更新をテストする追加の時間が得られます。

### <a name="what-happens-when-the-service-update-is-complete"></a>サービスの更新が完了するとどうなりますか。

サービス更新が Microsoft によって適用されると、更新が成功したか、適用できなかった場合に通知を受け取ります。  更新プログラムを適用できないいくつかの理由があります。

- 保留中のパッケージ サインオフ - パッケージがサインオフで保留中の場合、Microsoft はサービスの更新を実稼働環境に適用しません。  
- 配置エラー - 配置エラーが発生した場合、環境は元の状態にロールバックされます。
 
### <a name="if-there-is-a-failure-can-i-reschedule-the-update-to-be-auto-applied"></a>失敗した場合、更新プログラムが自動的に適用されるようにスケジュールを再設定できますか。

更新プログラムを再スケジュールすることはできませんが、他の更新プログラムの適用をスケジュールするのと同じように、都合の良いときにパッケージを適用することができます。

### <a name="will-critical-hotfixes-be-automatically-applied-to-my-sandbox-production-environment-during-auto-update"></a>重要なホットフィックスは、自動更新中にサンドボックス環境や実稼働環境に自動的に適用されますか。

一般提供されてすべての顧客に自動適用されるサービスの更新には、修正プログラムや潜在的な新しい機能が含まれます。  サービスの更新が適用された後に重要な問題点が報告されると、顧客は Lifecycle Services のタイルから累積的な修正プログラムを取り込むことができます。  

### <a name="how-will-my-isvs-stay-current"></a>私の ISV は常に最新ですか?

お客様の環境のサービスの更新には下位互換性があるため、独立系ソフトウェア ベンダー (ISV) によるアクションは必要ありません。 ISV は、そのコードが依存する最低限必要なプラットフォーム リリースを開発します。 重大な変更については、ISVが追加して検証するための 12 か月のリード タイムがあります。 ISV は、プラットフォーム ビットへの早期アクセスを獲得して、一般的に使用できるようになる前に更新プログラムに対するソリューションを検証できるようにするために、[パートナー早期アクセス プログラム](https://experience.dynamics.com/insider/)の一部とすることをお勧めします。

### <a name="what-about-new-features"></a>新機能はどうなりますか?

すべての新機能は 12 か月間オプトインとなり、機能の有効化を選択するまで変更管理は必要ありません。

### <a name="are-batch-jobs-suspended-during-a-service-update"></a>バッチ ジョブは、サービスの更新中に中断されますか?

バッチ ジョブはメンテナンス ウィンドウ中に中断され、メンテナンスの完了時に再開します。

## <a name="tools"></a>ツール

### <a name="how-can-i-get-early-access-to-non-released-platform-updates"></a>非リリースのプラットフォーム更新プログラムへの早期アクセスをどのように取得できますか。

[初回リリース プログラム](https://experience.dynamics.com/insider/)に参加できます。Microsoft は、常に最新の更新プログラムによってシステムを最新の状態に保ちます。 まだ Dynamics 365 Insider プログラムのメンバーとなっていない場合、次の作業が必要です。

1. この URL を使用してインサイダー プログラムにサインアップする: https://experience.dynamics.com
2. Dynamics 365 Insider になるための条件に同意します。
3. 申請が承認された後 (約 24 時間)、Insider Portal にサインインして、参加できるさまざまなプレビュー プログラムを検索することができます。 
4. プレビュー アーリー アクセス プログラム (PEAP) と初回リリース: プログラムに参加するには追加の使用条件に同意する必要があります。 ノミネートが受け入られた後、Dynamics 365 Insider プログラム内でこれらのプログラムを参照してください。

### <a name="is-there-tooling-available-to-support-testing-the-latest-release"></a>最新のリリースのテストをサポートするために使用可能なツールはありますか?

[Regression Suite Automation Tool](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests) は[現在利用可能](https://www.microsoft.com/download/details.aspx?id=57357)です。 このツールは、ユーザー受け入れテストの費用と時間を大幅に減少します。 通常、ユーザー受け入れテストは Microsoft アプリケーションの更新プログラムを取得するか、カスタム コードおよびコンフィギュレーションを実稼働環境に適用する前に必要です。 機能パワー ユーザーがタスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくても自動テストのスイートに変換できるようにします。 テスト ライブラリは、ビジネス プロセス モデラー (BPM) ライブラリを使用して Lifecycle Services に保存および配分され、テストの実行、報告、調査のために Azure DevOps と完全に統合されます。 テスト データ パラメーターは、テスト ステップから切り離され、Excel データ ファイルに保存されます。

### <a name="how-can-i-test-and-validate-that-the-integrations-continue-to-work"></a>統合が機能し続けていることはどのようにテストおよび検証できますか?

データ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証することができます。 また、タスクの結果の検証を使用して、データ エンティティの自動テストを使用することもできます。 詳細については、[データ タスクの自動化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-task-automation)トピックの差し込みデータの概要を参照してください。

### <a name="how-can-i-determine-whats-changed-in-a-service-update"></a>サービス更新プログラムの変更内容はどのようにわかりますか?

「新機能および変更された機能」ドキュメントは、各サービス更新に含まれている詳細の主要ソースです。 [リリース プラン](https://docs.microsoft.com/business-applications-release-notes/) は、今後のリリースのすべての新機能と変更の情報の主要ソースです。 必要に応じて、機能には docs.microsoft.com のヘルプ トピックも含められます。 影響分析ツールは、使用する機能への影響を理解するために LCS で利用可能になります。

### <a name="how-will-i-know-if-there-is-a-deprecated-feature-that-will-impact-me-if-im-not-doing-active-development-recompile-my-code"></a>現在開発中でない、またはコードを再コンパイルしない場合、推奨されない機能があるかどうかはどうすればわかりますか。 

非推奨の機能については、リリースのたびに記載されます。  詳細については、[削除済みまたは非推奨の機能](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features?toc=/fin-and-ops/toc.json) を参照してください。  

## <a name="preparing-for-one-version"></a>1 つのバージョンの準備

### <a name="how-can-i-log-an-extensibility-request"></a>拡張機能の要求を記録するにはどうすればよいですか?

拡張機能の要求は、LCS に記録することができます。 詳細は、[機能拡張要求](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/extensibility-requests)トピックにあります。 使用可能な拡張機能をログに記録して使用するには、以下のタイムライムに注目してください。

| 日         | 拡張性の要求 |
|--------------|------------------------|
| 2019 年 1 月 | 拡張機能のすべての要求は、2019 年 1 月 1 日までにログインする必要があります。 ISV とユーザーは、この時点までにコードを分析し、これらの要求を行うことが要求されます。 要求が 2019 年 1 月 1 日までに提出されない場合、2019 年 4 月より後に 7.3 を維持するための例外は提供されません。 |
| 2019 年 12 月 | 2019 年 1 月 1 日によって記録された要求については、拡張機能は 2019 年 12 月 31 日以前に入手可能になります。 これらの拡張機能を使用しているユーザーは、2020 年 4 月までに現在のバージョンに移行する必要があります。 |

### <a name="what-does-end-of-service-mean"></a>サービスの終了にはどのような意味がありますか?

Microsoft は、サービスの終了に達しているバージョンの問題を修正しません。 Microsoft は、3 サービス更新より古いバージョンで発生した問題の調査とトラブルシューティングも行いません。 サービスの終了に達したバージョンで問題が発生した場合は、最新の更新プログラムに更新し、それでも問題が解決されない場合は、その問題を報告する必要があります。

すべての環境は、引き続き Microsoft によって運用されます。 監視や自動修復など、環境に関するすべての自動プロセスも、環境がサポートされているバージョンである限り、引き続きそのままです。

### <a name="will-individual-hotfixes-be-supported"></a>個別の修正プログラムをサポートしますか?

8.1 以降、個別の修正プログラムはサポートされません。 ユーザーは、最新の累積的な更新プログラムに更新して修正プログラム (8.1.1 など) を適用する必要があります。 さらに、重要な修正プログラムは累積的であり、LCS サービス エクスペリエンスを通じて使用可能になります。

### <a name="will-you-notify-me-about-critical-hotfixes-released-for-the-monthly-update-that-im-on"></a>利用している毎月の更新プログラムに関してリリースされる重要は修正プログラムに関する通知は送信されますか。 

顧客が報告した問題は、Lifecycle Services 問題検索で検索できます。  未解決の問題が解決されたときに通知を受けるようにサインアップすることができます。  

### <a name="how-can-i-upgrade-to-8x"></a>8.x にアップグレードする方法を教えてください。

最新のアプリケーションにアップグレードする方法については、[最新の更新プログラムに移行するためのプロセス](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/upgrade-latest-update#scenario-3-upgrade-to-the-latest-application-release-1)を参照してください。 [8.0 から 8.1 への](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/appupdate-80-81)更新では、データのアップグレードは不要です。ダウンタイムが大幅に削減されるセルフ サービスの更新になります。

## <a name="commerce-service-updates"></a>コマース サービスの更新

### <a name="what-options-are-available-to-minimize-impact-to-my-commerce-cloud-components"></a>コマース クラウド コンポーネントへの影響を最小限に抑えるためにどのオプションを使用できますか?

コマース クラウド コンポーネントには、Dynamics 365 バックオフィスと同じダウンタイムが必要です。 今後のリリースでは、展開への更新を減らしてさらにスケジュールするために Retail Cloud Scale Unit (RCSU) が使用可能になります。 RCSU の詳細については、[ドキュメント](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-retail/planned-features)および[リリース ノート](https://docs.microsoft.com/business-applications-release-notes/#pivot=products&panel=products1) サイトにある発行済みのリリース情報を参照してください。

### <a name="will-there-be-options-to-take-individual-hotfixes-for-my-commerce-solution-components"></a>コマース ソリューション コンポーネントの個別の修正プログラムを取得するオプションはありますか?

コマース コンポーネントのすべての修正プログラムは累積的です。

### <a name="what-are-the-maintenance-downtime-requirements-that-may-impact-channel-operations"></a>チャンネル工程に影響を与える可能性のある保守ダウンタイム要件は何ですか?

冗長性の業務ニーズがある小売業者のため、Modern POS オフライン機能では、インターネットから切断中またはクラウド環境の更新中にコア POS 処理を使用できます。 Commerce Scale Unit を運用している店舗では、サポート クラウド メンテナンス期間中もコア POS 処理のサポートを伴う処理を継続します。 詳細については、[オンラインおよびオフライン販売時点管理 (POS) 処理](../../../retail/pos-operations.md)を参照してください。

### <a name="when-will-i-need-to-update-my-in-store-components"></a>店舗内コンポーネントを更新する必要があるのはいつですか?

店舗内のすべてのコンポーネントは、サポートを維持するために、1 年以内にリリースされたソフトウェアを実行している必要があります。 ユーザーには、自己ホスト コンポーネントを更新し (店舗かプライベートで管理するデータ センターにインストールされているコンポーネントなど)、これらのコンポーネントのインストールされているバージョンが積極的にサポートされていることを確認する責任があります。

### <a name="will-there-continue-to-be-backward-compatibility-for-the-in-store-components"></a>店舗内コンポーネントの下位互換性は続行されますか?

クラウドにホストされているコンポーネントの更新では、そのバージョンのリリース日から 12 か月間、小売業者によって自己ホストされるコンポーネント バージョンとの下位互換性が保持され続けます (店舗またはプライベート データ センターにインストールされているコンポーネントなど - Modern Point of Sale、Commerce Scale Unit、Hardware Station)。 自己ホストされているコンポーネントは、クラウドでホストされているコンポーネントと同時に更新する必要はなく、独立したリズムで更新できるため、店舗に更新を展開する時間があります。

### <a name="what-options-are-available-for-updating-in-store-components-across-my-organization"></a>組織全体で店舗内コンポーネントを更新するためにどのようなオプションを使用できますか?

ユーザーは、店舗ごとに手動で自己ホストされているコンポーネントを更新するか、Microsoft System Center Configuration Manager、Microsoft Intune などの一括更新ツールを使用するかを選択できます。

### <a name="what-options-do-i-have-to-slowly-enable-new-functionality-across-my-channels"></a>チャネル全体で新しい機能を徐々に有効にするどのようなオプションがありますか?

Microsoft では、店舗、デバイス、およびユーザー全体で機能拡張を徐々に展開して有効にするいくつかのメカニズムを提供しています。

- **画面レイアウト デザイナー**: POS のほとんどのビジュアル要素は、顧客組織の管理ユーザーによって構成され、集中管理されます。 つまり、対応する画面レイアウトに含まれるように明示的に設定されていない限り、新しい POS の操作は POS に自動的に表示されません。 画面レイアウトは、画面レイアウト デザイナーを使用して構成され、店舗または POS デバイスに固有の場合があります。 詳細については、[販売時点管理 (POS) の画面レイアウト](../../../retail/pos-screen-layouts.md)を参照してください。
- **機能プロファイル、POS のアクセス許可、コマース パラメーター** – POS の機能の重要な要素は通常、ユーザーがコンフィギュレーション可能です。 これは、機能プロファイル、POS のアクセス許可、コマース パラメーター、または該当するシナリオにおけるデバイス、レジスター、店舗、またはユーザー レベルの機能の管理を可能にするその他のコントロールを通じて設定できます。
- **Modern POS および Commerce Scale Unit** – Modern POS および Commerce Scale Unit は小売業者によって自己ホストされるため、いずれかのコンポーネントを含むトポロジによっては、個別 (および低速) のリズムかつクラウド専用トポロジより細かい方法での更新の展開が可能になります。

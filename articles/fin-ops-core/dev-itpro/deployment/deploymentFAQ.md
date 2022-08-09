---
title: セルフサービス配置の FAQ
description: この記事では、セルフサービス配置に関してよくある質問に対する回答を示します。
author: rashmansur
ms.date: 11/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d23d179c5bc60e70ee7ea6958df7b2484475fc05
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103550"
---
# <a name="self-service-deployment-faq"></a>セルフサービス配置の FAQ

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

この記事では、[セルフサービス配置](infrastructure-stack.md) に関してよくある質問に対する回答を示します。 シナリオがここにない場合は、[既知の問題](known-issues-new-deployment-experience.md)を参照してください。  

## <a name="why-do-i-see-only-application-version-811-and-platform-update-21-and-above-when-i-try-to-deploy-my-sandbox-environment-using-self-service-deployment"></a>セルフサービス配置を使用してサンドボックス環境を配置しようとすると、アプリケーション バージョン 8.1.1 とプラットフォーム更新 21 以上しか表示されないのはなぜですか? 

現時点では、セルフ サービス配置では、アプリケーション バージョン 8.1.1 とプラットフォーム更新 21 以上のみサポートされています。  

## <a name="my-development-environment-is-on-application-version-81-am-i-still-able-to-move-my-customization-to-the-sandbox-environment"></a>開発環境では、アプリケーション バージョン 8.1 です。 それでもサンドボックス環境にカスタマイズを移動できますか? 

はい。 アプリケーション バージョン 8.1.1 は、アプリケーション 8.1 と完全に下位互換があります。 

## <a name="what-is-the-minimum-supported-application-and-platform-version-when-trying-to-use-the-self-service-deployment"></a>セルフサービス配置を使用する場合、アプリケーションとプラットフォームのサポートされている最小バージョンは何ですか? 

プラットフォーム更新 20 を搭載したアプリケーション バージョン 8.1 が、最小のサポートされているバージョンです。 

## <a name="what-do-i-do-if-deployment-fails"></a>配置が失敗した場合どうしたらよいですか? 

1. 配置を削除してください。  
2. 同じ環境名を再利用する場合、5 分待機してからやり直してください。 それ以外の場合、新しい名前で配置を再実行してください。 
3. 配置が再度失敗した場合は、サポート チケットを記録してください。  

> [!Note]
> Microsoft は、今後のリリースで自動再試行ロジックを追加し、ログを使用できるようにします。 

## <a name="what-if-my-deployment-fails-with-an-environment-already-exists-error"></a>"既に環境が存在する" エラーが発生すると配置はどうなりますか? 

削除したばかりの配置の環境名を再利用できます。 配置を再試行する前に、5 ～ 10分間待ってください。 

## <a name="i-dont-have-remote-desktop-access-to-my-sandbox-environment-how-do-i-perform-critical-actions-that-require-remote-desktop-access-today"></a>サンドボックス環境へのリモート デスクトップ アクセス権がありません。 現在リモート デスクトップ アクセスを必要とする重大なアクションはどうすれば実行できますか?

Microsoft リモート デスクトップ アクセスはなくなりますが、引き続きレベル 2 以上のサンドボックス環境を操作できます。ここで説明している共通の重要なアクションを実行するために使用できる、セルフサービスの機能とツールが Microsoft により用意されているためです。

### <a name="access-the-azure-sql-database"></a>Azure SQL データベースにアクセスする
次の手順に従って、Microsoft Azure SQL データベースにアクセスすることができます。

1. LCS から、SQL Management Studio を使用して Azure SQL データベースに接続に使用するコンピューターの IP アドレスをセーフ リストに追加します。
2. LCS を使用して、データベース資格情報を参照するアクセスを要求します。 アクセスを要求する理由を提示する必要があります。 

要求を送信するとすぐに自動的に承認されます。 1 分または 2 分以内に、LCS 環境の詳細ページでデータベース アクセスの資格情報を確認できるようになります。 SQL データベースに接続するために資格情報を使用することができます。

> [!NOTE]
> 資格情報は 8 時間有効です。その後、有効期限が切れます。 資格情報の有効期限後、もう一度アクセス権を要求する必要があります。 

### <a name="access-log-files"></a>ログ ファイルへのアクセス
すべてのログ ファイルは、LCS 環境監視ページの **活動** タブから表示してダウンロードできます。

### <a name="use-perfmon-tools"></a>perfmon ツールを使用する
リモート デスクトップを使用できなくなるため、パフォーマンスの問題を診断するために perfmon.exe を使用できなくなりますが、LCS を通じて CPU およびメモリ消費の重要な稼働状態メトリックを監視することができます。 さらに、事前定義されたクエリをオンデマンドで実行でき、レベル 2 以上の環境でのパフォーマンスの問題を軽減するために事前に定義されたアクションを実行することができます。 

### <a name="access-self-service-logs"></a>セルフサービス ログにアクセスする
LCS を通じて環境で実行されるセルフサービス操作に関連するすべてのログは、LCS からダウンロードできます。 これらのセルフサービス操作には、配置、処理、およびデータベースの移動が含まれます。 LCS 環境履歴ページからログ フォルダーをダウンロードすることができます。

### <a name="turn-maintenance-mode-onoff"></a>メンテナンス モードのオン/オフを切り替える
2019 年 1 月リリースから、LCS でのセルフサービスの操作によって環境内のメンテナンス モードをオン/オフできるようになります。

### <a name="restart-services"></a>サービスをリセット
2019 年 1 月リリース以降、LCS のセルフサービス アクションによりサービスを再起動できるようになります。

### <a name="configure-the-regression-suite-automation-tool"></a>Regression Suite Automation Tool を構成する
マイクロソフトは、リモート デスクトップを使用しなくても wif.config ファイルの証明書サムネイルを更新できるようにするツールを作成中です。 このツールは、2019 年 2 月にリリースされる予定です。 それより前に Regression Suite Automation Tool を使用する必要がある場合は、サポート リクエストを記録してください。

## <a name="i-must-perform-one-of-the-critical-actions-that-are-listed-earlier-in-this-article-but-the-self-service-feature-isnt-yet-available-how-do-i-get-help"></a>この記事の前方に一覧表示されている重大なアクションのいずれかを実行する必要がありますが、セルフサービス機能はまだ使用できます。 ヘルプを表示する方法を教えてください。

サポート チケットを記録すると、Microsoft が環境でのアクションの実行をお手伝いします。

## <a name="i-dont-have-remote-desktop-access-to-my-sandbox-environment-and-the-critical-action-that-i-must-perform-isnt-listed-in-this-article-how-do-i-get-help"></a>サンドボックス環境にリモート デスクトップ アクセスがなく、実行する必要がある重要なアクションがこの記事に挙げられていません。 ヘルプを表示する方法を教えてください。

重要なアクションのこの記事の前方に掲載されていない場合、記事にコメントを追加するかドキュメンテーション バグを記録すると、Microsoft が要求に対応します。

## <a name="what-regions-are-supported-on-self-service-in-north-america"></a>セルフサービスがサポートされている北米の地域はどこですか?
現時点では、北米では次の地域のみサポートしています。

- 米国東部
- 米国西部
- 米国中部
  > [!NOTE]
  > 2021 年 4 月 1 日以降、セルフサービス移行のオプションとして米国中部は提供されなくなりました。

利用可能な地域の詳細については、[Dynamics 365 の国際的な可用性](https://www.microsoft.com/trustcenter/privacy/dynamics365-operations-location) を参照してください。

### <a name="my-environments-are-currently-in-the-regions-that-are-no-longer-supported-how-will-this-change-affect-me"></a>使用している環境は、サポートされなくなった地域にあります。 この変更にどのような影響がありますか?
2020 年 8 月 1 日以降にオンボードされたプロジェクトは、次の地域ではサポートされなくなりました。

-   米国東部 2
-   米国西部 2
-   西中央アメリカ
-   米国中北部
-   米国中南部

> [!NOTE]
> このことは、格納データが 2020 年 8 月以前に非推奨領域に保有されている環境には影響しません。 非推奨の地域の顧客を別の地域に移動するための移行計画があります。 サポートされている国と地域についての最新の一覧は、[Dynamics 365 の国際的な可用性](https://www.microsoft.com/trustcenter/privacy/dynamics365-operations-location)を参照してください。

- すべてのセルフサービス移行では、環境がホストされる地域の発信 IP アドレスを変更しています。 新しい発信 IP アドレスを使用できるので、今後のセルフサービス移行の前に追加する必要があります。 IP アドレスの詳細については、「[Microsoft が管理する環境では、外部コンポーネントが明示的な発信 IP セーフ リストに依存しています。セルフサービス導入への移行後に、サービスに影響がないことを確認するにはどうすればよいですか?](deploymentFAQ.md#for-my-microsoft-managed-environments-i-have-external-components-that-have-dependencies-on-an-explicit-outbound-ip-safe-list-how-can-i-ensure-my-service-is-not-impacted-after-the-move-to-self-service-deployment)」を参照してください。
- 待機時間が原因で発生する統合やその他の依存関係があり、地域の変更による影響について質問がある場合は、[Microsoft サポート](../lifecycle-services/lcs-support.md) にお問い合わせください。
- 米国中部は、セルフサービス移行のオプションではなくなりました。 顧客が二重書き込み機能、仮想エンティティ、または Dataverse に依存する財務と運用アプリのアドインを利用する予定の場合、Dataverse は米国中部ではサポートされていないことに注意してください。 当面、米国中部で Dataverse をサポートする計画はありません。 サポートされている地域の機能を引き続き使用するために、お使いの環境を中部米国ではなく東部米国または西部米国に移行する計画です。
- 一部の環境でセルフサービス機能を使用しているプロジェクトが米国中部にあり、その他の環境では中北部、中南部、中西部にある場合でも、移行の一環として残りの IaaS 環境を米国東部または西部に移動できます。 Service Fabric 上および米国中部にすでに存在する環境については、Microsoft サポートに問い合わせて、必要に応じて米国東部/西部への移動を依頼してください。
-   現在のリージョンのすべての Azure リソースを確認し、移行の一環として今後の変更に備えて、新しいリージョンと同じ場所に配置する必要があるかどうかを評価してください。
- 地域間の移行に関連するデータ移動について質問がある場合は、[異なるインフラストラクチャ (Microsoft による管理対セルフ サービス) 上にあるソースおよびターゲット](../database/database-pitr-prod-sandbox.md#the-source-and-target-are-on-different-infrastructure-microsoft-managed-vs-self-service) を参照してください。

## <a name="for-my-microsoft-managed-environments-i-have-external-components-that-have-dependencies-on-an-explicit-outbound-ip-safe-list-how-can-i-ensure-my-service-is-not-impacted-after-the-move-to-self-service-deployment"></a>Microsoft が管理する環境には、明示的な発信 IP セーフ リストに依存関係がある外部コンポーネントがあります。 セルフサービス配置への移行後にサービスが影響を受けないようにするにはどうすればよいですか?
セルフサービス移行では、環境がホストされる地域の発信 IP アドレスを変更しています。 新しい発信 IP アドレスを使用して、今後のセルフサービス移行またはポスト移行の準備として追加することができます。

* 外部コンポーネントのいずれにも、IP アドレスの明示的な包含一覧、ルーティングまたはファイアウォールの発信 IP アドレスの特別な処理が依存していない場合、アクションは必要ありません。
* 外部コンポーネントのいずれかが AOS と通信するための発信 IP アドレスに対して特別な処理がある場合は、既存のものが表示される場所に新しい発信 IP アドレスを追加します。 既存の IP アドレスを置き換えないでください。 新しい発信 IP アドレスは、次の一覧にあります。 たとえば、発信 IP アドレスが AOS の外部のファイアウォールに明示的に含まれている場合や、外部サービスに、AOS の発信 IP アドレスを含む許可一覧が設定されている場合があります。

AOS への受信 IP アドレスが動的になります。 これにより、インフラストラクチャの変更が行われるたびに時間とともに変更します。

> [!NOTE]
> AOS からの発信 IP アドレスは、配置の Azure リージョンに基づく一覧の範囲からの IP アドレスになります。 特定の発信 IP アドレスは、同じセッション内からでも、送信要求ごとに異なる場合があります。

| 場所 | Azure リージョン | IP 接頭語<sup>1</sup> |
|---|---|---|
| アジア太平洋 | 東アジア | 52.229.231.64/26 |
| アジア太平洋 | 東南アジア | 20.44.247.0/26 |
| オーストラリア | オーストラリア東部 | 20.40.190.0/26 |
| オーストラリア | オーストラリア南東部 | 20.40.165.192/26 |
| Azure Government | US Gov テキサス <sup>2</sup> | 52.243.163.224/28 |
| Azure Government | US Gov バージニア | 52.227.253.160/28 |
| ブラジル | ブラジル南部 | 191.234.130.0/26 |
| カナダ | カナダ中部 | 20.151.60.0/26 |
| カナダ | カナダ東部 | 52.155.27.128/26 |
| 中国 | 中国東部 2 | 52.131.245.128/26 |
| 中国 | 中国北 2 | 52.130.157.64/26 |
| ヨーロッパ | 北ヨーロッパ | 52.155.160.192/26 |
| ヨーロッパ | 西ヨーロッパ | 20.61.88.128/26<br/>51.105.159.192/26 |
| フランス | フランス中央部 | 51.138.205.48/28 |
| フランス | フランス南部<sup>2</sup> | 52.136.140.96/28 |
| インド | インド中部 | 20.193.248.192/26 |
| インド | インド南部 | 20.40.5.0/26 |
| 日本 | 東日本 | 20.48.77.192/26 |
| 日本 | 西日本 | 20.39.179.192/26 |
| 南アフリカ | 南アフリカ北部 | 102.133.204.16/28 |
| 南アフリカ | 南アフリカ西部<sup>2</sup> | 102.133.78.96/28 |
| スイス | スイス北部 | 51.103.164.128/28 |
| スイス | スイス西部<sup>2</sup> | 51.107.230.128/28 |
| アラブ首長国連邦 | アラブ首長国連邦北部 | 20.203.41.96/28 |
| イギリス | イギリス南部 | 51.11.26.192/26 |
| イギリス | イギリス西部 | 51.137.139.0/26 |
| 米国 | 米国中部 | 13.86.98.128/26 |
| 米国 | 米国東部 | 52.255.218.64/26 |
| 米国 | 米国西部 | 52.250.195.128/26 |

<sup>1</sup> 西ヨーロッパなどの複数の IP 接頭語を持つ Azure リージョンでは、一覧に示されている任意の IP 接頭語 からの IP アドレスを発信要求で使用します。

<sup>2</sup> BCDR 専用の Azure リージョンを表します。 発信要求は、地域内で地域のフェイルオーバーの必要がある障害復旧のシナリオにあるこの地域からのみ発生します。

## <a name="what-does-the-downtime-look-like-for-self-service-migrations"></a>セルフサービス移行の場合、ダウンタイムはどのようになりますか?
セルフサービスによる移行では、どのような環境でも 3 時間の 100% ダウンタイムが発生しますが、移行前の 6 時間のウィンドウを経て、実際の移行時のダウンタイムは 3 時間となります。 この環境は、6 時間の移行前のウィンドウでは限られたサービス機能を使用できますが、3 時間の移行ウィンドウでは完全に使用できなくなります。 移行前のウィンドウでは、パッケージの展開などのサービスアクティビティをスケジュールしないことをお勧めします。これは、移行が妨げられ、移行のキャンセルが発生するためです。

## <a name="is-there-a-potential-impact-on-the-environments-certificates"></a>環境の証明書に影響が及ぶ可能性がありますか?

はい、以前の非セルフサービス配置から移行する場合、インフラストラクチャの違いによって環境の証明書が更新される場合があります。 ソリューション/統合の証明書に依存しているかどうかを判断し、移行後に必要なアクションを実行します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


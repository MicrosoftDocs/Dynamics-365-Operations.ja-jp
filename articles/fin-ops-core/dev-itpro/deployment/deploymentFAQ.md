---
title: セルフサービス配置の FAQ
description: このトピックでは、セルフサービス配置に関してよくある質問に対する回答を示します。
author: rashmansur
manager: AnnBe
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: c0db290d424203ccff3c152f15ca7601bf9b9f9c
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "5077680"
---
# <a name="self-service-deployment-faq"></a>セルフサービス配置の FAQ

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

このトピックでは、[セルフサービス配置](infrastructure-stack.md)に関してよくある質問に対する回答を示します。 シナリオがここにない場合は、[既知の問題](known-issues-new-deployment-experience.md)を参照してください。  

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

## <a name="i-must-perform-one-of-the-critical-actions-that-are-listed-earlier-in-this-topic-but-the-self-service-feature-isnt-yet-available-how-do-i-get-help"></a>このトピックの前方に一覧表示されている重大なアクションのいずれかを実行する必要がありますが、セルフサービス機能はまだ使用できます。 ヘルプを表示する方法を教えてください。

サポート チケットを記録すると、Microsoft が環境でのアクションの実行をお手伝いします。

## <a name="i-dont-have-remote-desktop-access-to-my-sandbox-environment-and-the-critical-action-that-i-must-perform-isnt-listed-in-this-topic-how-do-i-get-help"></a>サンドボックス環境にリモート デスクトップ アクセスがなく、実行する必要がある重要なアクションがこのトピックに挙げられていません。 ヘルプを表示する方法を教えてください。

重要なアクションのこのトピックの前方に掲載されていない場合、このトピックにコメントを追加するかドキュメンテーション バグを記録すると、Microsoft が要求に対応します。

## <a name="for-my-microsoft-managed-environments-i-have-external-components-that-have-dependencies-on-an-explicit-outbound-ip-safe-list-how-can-i-ensure-my-service-is-not-impacted-after-the-move-to-self-service-deployment"></a>Microsoft が管理する環境には、明示的な発信 IP セーフ リストに依存関係がある外部コンポーネントがあります。 セルフサービス配置への移行後にサービスが影響を受けないようにするにはどうすればよいですか?
セルフサービス移行では、環境がホストされる地域の発信 IP アドレスを変更しています。 新しい発信 IP アドレスを使用して、今後のセルフサービス移行またはポスト移行の準備として追加することができます。

* 外部コンポーネントのいずれにも、IP アドレスの明示的な包含一覧、ルーティングまたはファイアウォールの発信 IP アドレスの特別な処理が依存していない場合、アクションは必要ありません。
* 外部コンポーネントのいずれかが AOS と通信するための発信 IP アドレスに対して特別な処理がある場合は、既存のものが表示される場所に新しい発信 IP アドレスを追加します。 既存の IP アドレスを置き換えないでください。 新しい発信 IP アドレスは、次の一覧にあります。 たとえば、発信 IP アドレスが AOS の外部のファイアウォールに明示的に含まれている場合や、外部サービスに、AOS の発信 IP アドレスを含む許可一覧が設定されている場合があります。

AOS への受信 IP アドレスが動的になります。 これにより、インフラストラクチャの変更が行われるたびに時間とともに変更します。

> [!NOTE]
> AOS の発信 IP アドレスは、現在、2021 年 6 月で終了するように一覧表示されている個別の AOS セッションの期間中は、静的なままになります。 

| リージョン | IP 接頭語
|---------------------|-------------|
| 米国西部 | 52.250.195.128/26
| 米国東部 | 52.255.218.64/26
| 米国中部 | 13.86.98.128/26
| 西ヨーロッパ | 51.105.159.192/26
| 西ヨーロッパ -2 | 20.61.88.128/26
| 北ヨーロッパ | 52.155.160.192/26
| イギリス西部 | 51.137.139.0/26
| イギリス南部 | 51.11.26.192/26
| オーストラリア東部 | 20.40.190.0/26
| オーストラリア南東部 | 20.40.165.192/26
| カナダ中部 | 20.151.60.0/26
| カナダ東部 | 52.155.27.128/26
| ブラジル南部 | 191.234.130.0/26
| 東アジア | 52.229.231.64/26
| 東南アジア | 20.44.247.0/26
| 東日本 | 20.48.77.192/26
| 西日本 | 20.39.179.192/26

## <a name="is-there-a-potential-impact-on-the-environments-certificates"></a>環境の証明書に影響が及ぶ可能性がありますか?

はい、以前の非セルフサービス配置から移行する場合、インフラストラクチャの違いによって環境の証明書が更新される場合があります。 ソリューション/統合の証明書に依存しているかどうかを判断し、移行後に必要なアクションを実行します。

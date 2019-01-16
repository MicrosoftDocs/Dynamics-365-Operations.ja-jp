---
title: "セルフサービス配置の FAQ"
description: "このトピックでは、セルフサービス配置に関してよくある質問に対する回答を示します。"
author: sarvanisathish
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: aa3533a1ee22d5063db7e8bb66b03853056aa743
ms.openlocfilehash: 3130b00a0e925cd50da433c0c3602e675f416bf1
ms.contentlocale: ja-jp
ms.lasthandoff: 12/19/2018

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

1. LCS から、SQL Management Studio を使用して Azure SQL データベースに接続するために使用するコンピューターの IP アドレスをホワイトリストに追加します。
2. LCS を使用して、データベース資格情報を参照するアクセスを要求します。 アクセスを要求する理由を提示する必要があります。 

要求を送信するとすぐに自動的に承認されます。 1 分または 2 分以内に、LCS 環境の詳細ページでデータベース アクセスの資格情報を確認できるようになります。 SQL データベースに接続するために資格情報を使用することができます。

> [!NOTE]
> 資格情報は 8 時間有効です。その後、有効期限が切れます。 資格情報の有効期限後、もう一度アクセス権を要求する必要があります。 

### <a name="access-finance-and-operation-logs"></a>Finance and Operation ログにアクセスする
すべての Finance and Operations ログは、LCS 環境監視ページの **活動** タブから表示してダウンロードできます。

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


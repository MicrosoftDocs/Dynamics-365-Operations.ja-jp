---
title: 実装プロジェクト FAQ の Go-live
description: このトピックでは、実装プロジェクトの運用についてよく寄せられる質問を一覧表示します。
author: sshashi7
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: sshashi
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: d993168feebd98f4c4a90b692d64186ed53df20e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103877"
---
# <a name="go-live-for-implementation-projects-faq"></a>実装プロジェクト FAQ の Go-live

[!include [banner](../includes/banner.md)]

このトピックでは、実装プロジェクトの運用についてよく寄せられる質問を一覧表示します。

## <a name="when-can-i-configure-and-request-my-production-environment"></a>実稼働環境をいつ構成および要求できますか ?

通常、すべてのカスタマイズのコードが完了し、ユーザー受け入れテスト (UAT) が完了し、顧客がソリューションからサインオフし、稼働中にブロッキングの問題がない場合、実稼働環境が展開されます。

お客様がこの段階にいるとき、Microsoft FastTrack チームはプロジェクトチームと連携して、Go-live 評価/レビューを行ういます。

## <a name="what-are-the-prerequisites-to-deploy-a-production-environment"></a>実稼働環境を配置するための前提条件

前提条件の一覧については、 [Go-Live の準備](prepare-go-live.md) を参照してください。

## <a name="what-is-a-go-live-assessmentreview-and-why-is-it-required"></a>起動の評価/レビューとは何ですか、またそれがなぜ必要ですか ?

Go-live 評価/レビューは、[Microsoft FastTrack プログラム](/dynamics365/fasttrack/)の一部です。 レビュー中に、ソリューション アーキテクトは、実装プロジェクトが成功した切替および Go-live の準備が整っているかどうかを評価します。 このレビューは、実稼働環境で準備を開始する前に、すべての実装プロジェクトで必須です。

## <a name="i-want-to-request-my-production-environment-who-do-i-contact-for-a-go-live-assessmentreview"></a>実稼働環境を要求します。 Go-live アセスメント/レビューのために誰に連絡しますか。
FastTrack ソリューション アーキテクトがプロジェクトに割り当てられている場合は、担当者に直接問い合わせます。 それ以外の場合、Microsoft Dynamics Lifecycle Services (LCS) に指定されている運用日付に基づいて、運用前チェックリストに記入し、運用日の数週間前に <d365fogl@microsoft.com> に送信するように指示する電子メールを受信します。 電子メールを受信しておらず Go-Live の準備ができている場合は、[Go-live 計画 TechTalk](https://aka.ms/FastTrackPreGoLiveChecklist) ページの **Dynamics 365 コミュニティ** からチェックリストをダウンロードし、記入して d365fogl@microsoft.com に送信できます。

## <a name="the-production-button-isnt-available-in-lcs-how-do-i-request-my-production-environment"></a>生産ボタンは、LCS では使用できません。 実稼働環境を要求するにはどうすればよいですか。

LCS の **生産** ボタンは、LCS 実装方法の **分析**、**デザイン & 開発**、および **テスト** フェースを完了した後にのみ使用可能です。 これらのフェーズを完了する方法の詳細については、 [Finance and Operations アプリの顧客用の Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs-works-lcs.md) を参照してください。

> [!NOTE]
> 実稼働環境は、運用の評価/レビューが完了するまで配置されません。

## <a name="my-sandbox-environment-is-currently-on-an-update-that-is-set-to-expire-in-two-months-can-i-request-a-production-environment-that-has-the-latest-update"></a>自分のサンドボックス環境は、現在有効期限が 2 か月に設定されている更新プログラムにあります。 最新の更新プログラムを含む実稼動環境を要求できますか。

一連番号 サンド ボックス環境と異なるバージョンにある実稼働環境に対する要求をすべて拒否します。 実稼働環境をコンフィギュレーションするときは、選択したバージョンが、ソリューションを承認したサンド ボックス環境のバージョンと一致する必要があります。 したがって、まず最新の更新プログラムをサンドボックス環境に適用してテストし、サインオフする必要があります。

詳細については、 [ソフトウェアのライフサイクル ポリシーおよびクラウド リリース](../../dev-itpro/migration-upgrade/versions-update-policy.md) を参照してください。

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-but-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>サンドボックス環境は、米国中部データセンターに配置されますが、生産環境は米国西部データセンターに配置する予定です。 本番構成で、データ センターとして米国西部を選択できますか？

一連番号 サンド ボックス環境と異なるデータ センター内にある実稼働環境に対する要求をすべて拒否します。 すべての環境が同じデータ センターに配置されていることが必要です。 実稼働環境を米国西部データセンターに配置するには、まずサンドボックス環境を米国西部のデータセンターに再展開してテストし、サインオフする必要があります。

正しいデータ センターを選択するのに役立つ情報の詳細については、「システム要件」トピックの [ネットワーク要件](../get-started/system-requirements.md#network-requirements) セクションを参照してください。

## <a name="how-will-my-production-environment-be-sized"></a>実稼働環境はどのくらいの規模になりますか。

実稼働環境のサイズは、現在のユーザー ライセンス数と、実稼働環境を要求するときに有効なサブスクリプションの推定の情報に基づいて決まります。

> [!NOTE]
> 追加のユーザーを後で追加する場合は、新しいサブスクリプション推定をアクティブ化するためのサポート チケットを作成する必要があります。 実稼働環境のサイズは、ユーザー数、ユーザーのライセンスの種類、および予想されるピーク時のトランザクション量に応じて変更する必要があります。 ダウンタイムは、実稼働環境のサイズを変更するために必要です。

## <a name="i-submitted-the-request-for-a-production-environment-but-i-made-a-mistake-can-i-still-change-it"></a>実稼働環境の要求を送信しましたが、間違いが発生しました。 いまでも変更できますか。

はい。 実稼働環境のステータスが **キュー** に設定されている限り、サインオフ フラグをクリアし、変更、および再度サイン オフにすることができます。

## <a name="how-long-does-it-take-to-deploy-my-production-environment"></a>実稼働環境を配置するにはどのくらい時間がかかりますか。

Microsoft FastTrack チームによる Go-live アセスメントが完了し、生産要求が送信された後、48 時間内で実稼働環境の配置を完了する必要があります。

## <a name="what-level-of-access-do-i-have-in-my-production-environment-can-i-sign-in-to-the-vm"></a>自分の実稼動環境にて、どのレベルのアクセスが可能ですか。 VM にログインできますか。

一連番号 実稼働環境へのアクセスは制限されます。 仮想マシン (VM) または Microsoft インターネット インフォメーション サービス (IIS) にアクセスすることはできません。 また、Microsoft SQL Server Management Studio 経由でデータベースにアクセスすることはできません。

## <a name="how-often-is-my-production-database-backed-up"></a>どのくらいの頻度で生産データベースがバックアップされますか。

データベースは自動バックアップによって保護されています。 完全なデータベース バックアップは毎週行われ、差異のデータベース バックアップは毎時間行われ、およびトランザクション ログのバックアップは 5 分ごとに行われます。 自動バックアップは 28 日間保持されます。

詳細については、[自動 SQL データベースのバックアップについて](/azure/sql-database/sql-database-automated-backups) を参照してください。

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>生産データベースのバックアップのコピーを要求できますか。

一連番号 ただし、データベースの更新サービス要求を送信し、レベル 2 およびそれ以上の大きいサンドボックス環境に運用データベースをコピーすることができます。 コピー要求が完了した後、サンドボックス環境をバックアップすることができます。

## <a name="my-golden-configuration-database-is-in-a-tier-1-sandbox-environment-how-can-i-copy-and-restore-it-to-my-production-environment"></a>高品質の構成データベースは、第 1 層サンドボックス環境にあります。 実稼働環境にどのようにコピーおよび復元しますか。
データベースをコピーして復元するには、トピック [ゴールデンコンフィギュレーションプロモーション](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md) の指示に従います。 

> [!NOTE]
> 高品質の構成がデータ パッケージにある場合、実稼働環境に手動でデータ パッケージをインポートする必要があります。

## <a name="after-go-live-can-i-apply-new-code-changes-to-the-production-environment"></a>Go-Live の後、実稼働環境に新しいコード変更を適用することはできますか?

はい。 LCS で、配置可能パッケージを実稼働環境に適用するサービス要求を送信することができます。 1 つの配置可能パッケージのアプリケーションを実稼動環境に関与させると、5 時間のリード タイムと約 5 時間のダウンタイムになります。

詳細については、[クラウド環境への更新プログラムの適用](../../dev-itpro/deployment/apply-deployable-package-system.md)を参照してください。

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>実稼働環境がダウンした場合はどうすればよいでしょうか ?

稼働停止をレポートするには、トピック [稼働停止のレポート](../../dev-itpro/lifecycle-services/report-production-outage.md) で説明されているプロセスに従います。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: 優先順位に基づく調整に関する FAQ
description: このトピックでは、OData の優先度ベースのスロットリングとカスタムサービスベースの統合に関するよくある質問 (FAQ) に対する回答を提供します。
author: hasaid
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Platform update 37
ms.openlocfilehash: 11153abee99865f97b778c4304d0b8dcb7f2a4372c30a8dbfbfbe077a5bb3744
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764452"
---
# <a name="priority-based-throttling-faq"></a>優先順位に基づく調整に関する FAQ

[!include [banner](../includes/banner.md)]


このトピックでは、Open Data Protocol (OData) およびカスタム サービス ベースの統合に関する [優先順位に基づく調整](priority-based-throttling.md) に関するよく寄せられる質問 (FAQ) に対する回答を提供します。

## <a name="how-do-i-access-the-data-management-yammer-group"></a>Yammer グループのデータ管理にどのようにアクセスできますか?
データ管理 Yammer グループにアクセスするには、[データ管理 Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13408417) に移動します。

## <a name="when-will-throttling-be-enabled-by-default"></a>調整はいつ既定で有効になりますか?
調整機能は、Finance 10.0.13 以降にプレビューされており、バージョン 10.0.19 から既定で有効になります。 OData およびカスタム サービス リクエストの優先順位を設定することにより、環境に手動で調整をトリガーできます。 ただし、Finance 10.0.19 のリリース以降、優先順位を設定していなくても、調整は自動的に有効になります。

Finance バージョン 10.0.19 は、2021 年 4 月後半にプレリリースされる予定で、通常は 2021 年 6 月に一般的に利用可能になります。

## <a name="will-a-retry-request-receive-preferential-treatment-over-a-new-request"></a>再試行要求は新規要求より優先処理されますか?
いいえ。

## <a name="will-my-environment-be-subject-to-any-api-limits"></a>私の環境は API の制限対象になりますか?
いいえ。 現時点では、環境は API の制限対象ではありません。 

環境全体にわたるワークロードの影響を評価するために、テレメトリ データが収集されます。 このデータは、使用状況に基づく制限の導入のロードマップを定義する場合に、API のベースライン制限を確立するのに役立ちます。

## <a name="is-there-a-report-that-determines-when-throttling-might-occur"></a>調整が発生する時を決定するレポートがありますか?
はい。 レポートは利用可能で、LCS の **環境の監視** ページの **未加工ログ** からアクセスできます。 このビューに一覧表示される要求は、Finance バージョン 10.0.19 以降、この機能が既定でオンになっている場合に調整される可能性があります。

## <a name="will-throttling-affect-the-data-importexport-framework-dixf-and-batch"></a>調整はデータのインポート/エクスポート フレームワーク (DIXF) とバッチに影響しますか?
No. 調整は、Odata と カスタム サービス統合のためです。

## <a name="is-throttling-available-for-on-premises-environments"></a>オンプレミス環境で調整を使用できますか?
いいえ。 オンプレミス環境で調整は使用できません。

## <a name="in-preview-will-my-requests-be-throttled-if-priorities-arent-configured"></a>プレビューで、優先順位が構成されない場合、自分の要求は調整されますか?
いいえ、なぜならテレメトリのみが有効だからです。 実際の調整は、優先順位を構成した場合に実行されます。 プレビュー期間中は、**非実稼働** 環境でこのアプローチを使用することをお勧めします。

## <a name="can-throttling-be-enabled-on-dev-boxes"></a>開発ボックスで調整は有効にできますか?
いいえ。 優先順位を設定して、調整をトリガーできるのは、サンドボックス環境か実稼働環境のみです。

## <a name="what-happens-to-requests-if-the-user-didnt-retry-a-throttled-request"></a>ユーザーが調整された要求を再試行しなかった場合は、要求にどのような影響がありますか?
現時点では、429 エラーが発生して要求が再度実行されない場合、要求は処理されません。

## <a name="will-historic-throttling-information-be-used-to-advise-me-when-i-resize-environments"></a>環境のサイズを変更した場合、履歴の調整情報を使用して通知することができますか?
はい。 1 か月間、情報を Excel にエクスポートして、より詳細な分析やアーカイブを行うことができます。

## <a name="is-throttling-functionality-version-specific-if-it-is-which-version-is-it-available-in"></a>調整機能はバージョン固有ですか? その場合、どのバージョンで利用できますか?
優先順位に基づく調整は、Finance and Operations アプリのバージョン 10.0.13 以降のプレビューでご利用いただけます。

## <a name="are-there-plans-to-provide-an-option-for-the-priority-mapping-grid-entry"></a>優先順位マッピング グリッドのエントリにオプションを用意する計画はありますか?
この要求は、今後のリリースで考慮されます。

## <a name="will-the-requests-of-my-interactive-users-be-throttled"></a>対話型ユーザーの要求は調整されますか?
No. 対話型 (オンライン) ユーザーの要求には影響しません。

## <a name="if-i-experience-a-performance-issue-in-dynamics-365-finance-while-a-page-is-being-loaded-or-a-business-document-is-being-processed-how-does-that-performance-issue-differ-from-throttling"></a>ページが読み込まれているとき、またはビジネス ドキュメントが処理されているときに Dynamics 365 Finance でパフォーマンスの問題が発生した場合、そのパフォーマンスの問題は、調整とどのように異なりますか?
調整は、リソースの制約がある場合、システムを正常に管理する助けになります。 ページ アクションには影響しません。

## <a name="how-can-i-determine-the-wait-time-before-i-retry-a-throttled-request"></a>調整された要求を再試行するまでの待機時間をどのようにして決定できますか?
要求が調整された場合、再試行ロジックで時間を含めた回答ヘッダーを使用できます。 **再試行** HTTP ヘッダーを使用すると、秒単位で提供される値をでフェッチできます。 たとえば、**再試行: 60**。

## <a name="what-is-the-message-that-is-shown-as-part-of-the-429-http-response"></a>429 HTTP 応答の一部として表示されるメッセージは何ですか?
次のメッセージが表示されます。「システムのリソース稼働率が高いため、現時点ではこのリクエストを処理できませんでした。 要求を {0} 秒後に再試行します」。
**{0}** には，動的に計算された再試行サイクル間隔があります。

## <a name="does-throttling-apply-to-microsoft-services"></a>調整は Microsoft サービスに適用されますか?
Finance バージョン 10.0.19 以降では、以下の Microsoft サービスが最初は除外され、スロットリングは適用されません。 

   - ドキュメント回覧エージェント (DRA)
   - 倉庫モバイル (WHSMobile)
   - RetailAPI
   - Office 統合
   - データのインポート/エクスポート フレームワーク (DIXF)
   - データ インテグレーター
   - 二重書き込み
   - Finance and Operations アプリ- Power Platform 統合 (仮想エンティティ)
   - Finance and Operations アプリケーション コネクタ 

これらのサービスは除外されますが、テレメトリはこれらのサービスがシステム全体の正常性に与える影響とパフォーマンスについて収集されます。 

除外サービスの所有者は、2021 年度末までに 429 のハンドラーを実装することを優先しています。 その時点で、サービスはもはや除外されず、調整が適用されます。 これらの変更に先立って通知がなされ、ドキュメントが更新されます。

これらのサービスが独自のハンドラーを実装している場合でも、クライアント側の処理をお勧めします。 *再試行* ロジックを含む 429 のハンドラーの実装を検討してください。

## <a name="is-it-recommended-to-use-a-dedicated-integration-account-instead-of-just-the-generic-admin-user-account"></a>汎用管理者ユーザー アカウントの代わりに、専用の統合アカウントを使用することが勧められていますか?
はい、この方法を強く推奨します。 これらのサービス保護設定はユーザー固有の値に対して設定されているため、統合のほとんどまたはすべてに対して同じユーザー アカウントを使用すると、統合のニーズに対して相対的な優先順位を割り当てる機能が制限されます。 さらに、同じユーザー アカウントを使用すると、そのユーザー アカウントから発信されたすべての統合リクエストは調整の対象になります。

## <a name="does-throttling-depend-on-the-tier-that-my-environment-is-running-on"></a>調整は、自分の環境で実行している層によって異なりますか?
初期のリリースでは、いいえです。 調整は、各環境の使用可能なリソースに基づき、しきい値を計算します。

## <a name="is-throttling-functionality-legal-entityspecific"></a>調整機能は法人固有のものですか?
No.

## <a name="does-throttling-affect-bring-your-own-database-byod-export"></a>調整は、自分のデータベースの持ち込み (BYOD) エクスポートに影響を与えますか?
No.

## <a name="will-throttling-monitoring-be-available-in-application-insights"></a>調整監視は Application Insights で使用できるようになりますか?
将来、監視は使用可能な任意のツールにオンボーディングされます。

## <a name="if-a-production-environment-regularly-runs-out-of-resources-will-microsoft-have-to-resize-it"></a>運用環境が定期的にリソースを使い果たす場合、Microsoft はサイズ変更をする必要がありますか?
はい。 サイズ変更見積もりも再検証され、アップロードされます。

## <a name="after-april-2021-will-the-system-be-able-to-override-priority-based-throttling"></a>2021 年 4 月以降、システムは優先順位に基づく調整を上書きできますか?
システムは、2021 年 4 月以降優先順位が構成されない場合、既定値を使用します。

## <a name="can-the-throttling-engine-be-configured-thresholds"></a>調整エンジンは構成できますか (しきい値)?
No.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

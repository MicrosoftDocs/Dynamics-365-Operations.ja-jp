---
title: 優先順位に基づく調整に関する FAQ
description: このトピックでは、OData およびカスタム サービス ベースの統合の優先順位に基づく調整に関するよく寄せられる質問 (FAQ) に対する回答を提供します。
author: hasaid
ms.date: 09/23/2020
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
ms.openlocfilehash: b986414a4b85a749786761d955a7886c8efa97b0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749658"
---
# <a name="priority-based-throttling-faq"></a>優先順位に基づく調整に関する FAQ

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、Open Data Protocol (OData) およびカスタム サービス ベースの統合の[優先順位に基づく調整](priority-based-throttling.md) に関するよく寄せられる質問 (FAQ) に対する回答を提供します。

## <a name="how-do-i-access-the-data-management-yammer-group"></a>Yammer グループのデータ管理にどのようにアクセスできますか?

次のリンクを参照してください: [Yammer グループのデータ管理](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13408417)。

## <a name="will-a-retry-request-receive-preferential-treatment-over-a-new-request"></a>再試行要求は新規要求より優先処理されますか?

No.

## <a name="is-there-a-report-that-determines-when-throttling-might-occur"></a>調整が発生する時を決定するレポートがありますか?

はい。 レポートは提供され、Microsoft Dynamics Lifecycle Services (LCS) の環境監視ページ内の **未加工ログ** を通してアクセスできます。

## <a name="will-throttling-affect-the-data-importexport-framework-dixf-and-batch"></a>調整はデータのインポート/エクスポート フレームワーク (DIXF) とバッチに影響しますか?

No. 調整は、Odata と カスタム サービス統合のためです。

## <a name="in-preview-will-my-requests-be-throttled-if-priorities-arent-configured"></a>プレビューで、優先順位が構成されない場合、自分の要求は調整されますか?

いいえ、なぜならテレメトリのみが有効だからです。 実際の調整は、優先順位を構成した場合に実行されます。 プレビュー期間中は、**非実稼働** 環境でこのアプローチを使用することをお勧めします。

## <a name="what-happens-to-requests-if-the-user-didnt-retry-a-throttled-request"></a>ユーザーが調整された要求を再試行しなかった場合は、要求にどのような影響がありますか?

現時点では、429 エラーが発生して要求が再度実行されない場合、要求は処理されません。

## <a name="will-historic-throttling-information-be-used-to-advise-me-when-i-resize-environments"></a>環境のサイズを変更した場合、履歴の調整情報を使用して通知することができますか?

はい。 1 か月間、情報を Excel にエクスポートして、より詳細な分析やアーカイブを行うことができます。

## <a name="is-throttling-functionality-version-specific-if-it-is-which-version-is-it-available-in"></a>調整機能はバージョン固有ですか? その場合、どのバージョンで利用できますか?

優先順位に基づく調整は、**Finance and Operations アプリ** リリース バージョン 10.0.13 のプラットフォーム更新プログラムからプレビューでご利用いただけます。

## <a name="are-there-plans-to-provide-an-option-for-the-priority-mapping-grid-entry"></a>優先順位マッピング グリッドのエントリにオプションを用意する計画はありますか?

この要求は、今後のリリースで考慮されます。

## <a name="will-the-requests-of-my-interactive-users-be-throttled"></a>対話型ユーザーの要求は調整されますか?

No. 対話型 (オンライン) ユーザーの要求には影響しません。

## <a name="if-i-experience-a-performance-issue-in-dynamics-365-finance-while-a-page-is-being-loaded-or-a-business-document-is-being-processed-how-does-that-performance-issue-differ-from-throttling"></a>ページが読み込まれているとき、またはビジネス ドキュメントが処理されているときに Dynamics 365 Finance でパフォーマンスの問題が発生した場合、そのパフォーマンスの問題は、調整とどのように異なりますか?

調整は、リソースの制約がある場合、システムを正常に管理する助けになります。 ページ アクションには影響しません。

## <a name="how-can-i-determine-the-wait-time-before-i-retry-a-throttled-request"></a>調整された要求を再試行するまでの待機時間をどのようにして決定できますか?

要求が調整された場合、再試行ロジックで時間を含めた回答ヘッダーを使用できます。

## <a name="do-you-recommend-that-i-use-a-dedicated-integration-account-instead-of-just-the-generic-admin-user-account"></a>汎用管理者ユーザー アカウントの代わりに、専用の統合アカウントを使用することが勧められていますか?

はい、この方法をお勧めします。 ただし、必須ではありません。

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
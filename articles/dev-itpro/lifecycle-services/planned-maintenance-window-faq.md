---
title: 予定された保守ウィンドウのよく寄せられる質問
description: このトピックでは、Microsoft の計画されたメンテナンス ウィンドウに関するよくある質問に対する回答を示します。
author: manalidongre
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 6154
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a3e03e942aada5e7e41f11705b16c1bae92e132
ms.sourcegitcommit: c19d9cb1f1e77ce96ac4ec6e3212bc3c06288a7d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/23/2019
ms.locfileid: "892570"
---
# <a name="planned-maintenance-window-faq"></a>予定された保守ウィンドウのよく寄せられる質問
[!include [banner](../includes/banner.md)]

### <a name="what-is-a-planned-maintenance-window"></a>計画されているメンテナンス期間とは何ですか ?
メンテナンス予定期間は、機器設備や [サービス](../../fin-and-ops/get-started/one-version.md) に関する重要な更新を適用するために Microsoft がスケジュール設定をした時間枠です。

### <a name="how-does-a-planned-maintenance-window-work"></a>計画されているメンテナンス ウィンドウはどのように機能しますか。
すべての計画されたメンテナンスにつきましては、パッチ適用枠が開始する **5営業日** 前に Microsoft からすべての関係者にお知らせを送信します。 パッチ適用枠は環境にパッチが適用される期間です。 それは地理的な地域によって定義されます。 保守活動に関する詳細は、関係者に送信される通知に含まれます。

### <a name="when-is-this-planned-maintenance-window-taken"></a>この計画済みメンテナンス ウィンドウはいつ使用されますか ?
ユーザーへの影響を制限するため、環境が配置されている地域に応じてメンテナンス ウィンドウが予定されています。 次のリストは、各地域のメンテナンス ウィンドウを示しています。 すべての環境は、これら 3 つの地域のいずれかに分類されます。 時間は協定世界時 (UTC、グリニッジ標準時) で表示されます。

- **NAM:** 午前 2 時から午前 10 時
- **EMEA:** 午後 10 時から午前 6 時
- **APAC:** 午後 12 時から午後 9 時

### <a name="will-the-maintenance-from-microsoft-require-any-uptake"></a>Microsoft からの保守では何かを取得することが必要ですか。
ほとんどの保守作業でユーザー側のアクションは不要です。 取得が必要な重要なセキュリティ更新プログラムがある場合は、通知されます。

### <a name="who-will-be-notified-about-the-upcoming-planned-maintenance"></a>将来の計画的なメンテナンスはだれに通知されますか。
次の利害関係者には、今後のメンテナンスについて通知されます。

- プロジェクト所有者
- 組織の管理者
- 環境管理者
- デプロイ中または Microsoft Dynamics Lifecycle Services (LCS) で環境の詳細ページにある **通知する** ボタンによりリストに指定されたその他のユーザー。

### <a name="how-do-i-sign-up-to-be-notified-about-the-maintenance-window"></a>メンテナンス ウィンドウに関して通知を受け取るよう登録するにはどうすればよいですか。
任意のパートナー、独立系ソフトウェア仕入先 (ISV)、および次回の更新プログラムについて通知を受けたいその他の関係者は、関連する利害関係者 (プロジェクト所有者、環境管理者、または追加の関係者) として LCS プロジェクトに追加するよう依頼できます。

### <a name="why-cant-these-updates-be-applied-in-zero-downtime"></a>これらの更新プログラムがゼロ ダウンタイムで適用できないのはなぜですか。
Microsoft はサービスのダウンタイムの必要性を減らすよう継続的に努力しており、多くの定期的な保守作業ではダウンタイムを発生しません。 しかし、予測可能性を保証するため、Microsoft はゼロ ダウンタイムですべてのパッチを実行することはまだできません。

## <a name="microsoft-service-updates"></a>Microsoft のサービス更新プログラム 
別のよく寄せられる質問 (FAQ) に Microsoft によって行われるサービス更新プログラムに関する詳細が記載されています。 [1 つのバージョンのサービス更新プログラムに関してよく寄せられる質問](../../fin-and-ops/get-started/one-version.md) を参照してください。

## <a name="infrastructure-updates"></a>機器設備の更新 

### <a name="how-long-is-the-maintenance-window"></a>メンテナンス ウィンドウの長さはどの程度ですか。
ほとんどのオペレーティング システム レベルの更新は約 1 時間で完了します。 ただし、障害を処理してシステムを正常な状態に戻す時間があるため、Microsoft は 3 時間の時間枠を要求しています。 

すべてのアップデートの正確なダウンタイムは、アップデート開始前に通知されるメンテナンス ウィンドウ通知電子メールに含まれます。

### <a name="where-can-i-learn-more-about-what-is-applied"></a>何が適用されたかについての詳細はどこですか。
適用される更新プログラムの詳細については、[Microsoft セキュリティ速報](https://technet.microsoft.com/security/bulletins.aspx) を参照してください。

### <a name="where-can-i-track-progress-of-the-update"></a>更新プログラムの進捗はどのように追跡できますか。
オペレーティング システム レベルの更新中に、LCS は現在どのパッチ適用が進行中であるかを示しません。 ただし、Microsoft はこの機能をある時点で追加する予定です。

### <a name="what-environments-are-updated"></a>なんの環境が更新されるか。
オペレーティング システム レベルの更新は、Microsoft の基本サービスの一部として含まれているすべての第 2 層のサンドボックス環境に適用されます。 購入済のアドオンにも適用されます。 ただし、第 1 層サンドボックスおよびデモ環境など、他のすべての環境は顧客やパートナーの担当であることに注意してください。

### <a name="what-notifications-will-i-receive-about-upcoming-planned-maintenance"></a>次回の計画済みメンテナンスに関してどのような通知を受け取りますか ?
更新が予定されている 5 日前に、電子メール通知を受け取ります。 この電子メールには、更新される環境、更新の種類、更新が実行する見積もり時間、および実行する必要のある操作に関する情報が含まれます。

### <a name="will-i-be-notified-when-the-update-is-completed"></a>更新プログラムの完了時に通知されますか。
定義された保守時間枠で更新が完了する場合、更新が完了したときに通知を受信しません。 

### <a name="how-do-i-report-an-issue-that-is-identified-during-validation-of-the-updates-that-were-applied-to-the-environment"></a>環境に適用された更新の検証時に識別される問題をレポートするにはどうすればよいですか。
更新の検証中に特定された問題を報告するには、Microsoft にサポート チケットを提出し、タイトルに '予定された保守時間枠' を追加します。

### <a name="what-happens-if-the-patching-fails"></a>ファイルの修正に失敗した場合はどうなるでしょうか ?
修正が、オペレーティング システム レベル更新中に失敗すると、特定の修正プログラムはスキップされ、次の更新サイクルで適用されます。

### <a name="will-i-be-compensated-if-the-update-takes-longer-than-the-scheduled-maintenance-window"></a>更新プログラムが予定メンテナンス ウインドウより時間がかかる場合は補償されますか。
更新が予定された保守ウィンドウよりも長い場合は、余分な時間は予定外のダウンタイムと見なされ、一般的なサービス レベル アグリーメント (SLA) の対象となります。

### <a name="can-i-reschedule-the-planned-maintenance"></a>計画的なメンテナンスを再スケジューリングできますか。
Microsoft は計画的なメンテナンスを再スケジュールするためのオプションを提供していません。 ただし、現在の月の保守サイクルから除外するように選択できます。 

### <a name="how-do-i-opt-out-of-the-current-maintenance-cycle"></a>現在のメンテナンス サイクルを停止するにはどうすればよいですか。
現在のメンテナンス サイクルを無効にするには、Microsoft にサポート チケットを提出してください。 ご使用の環境は、今月の保守サイクルから除外されます。 ただし、お客様の環境は翌月に更新されます。

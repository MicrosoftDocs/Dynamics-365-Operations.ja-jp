---
title: 予定された保守ウィンドウのよく寄せられる質問
description: このトピックでは、Microsoft の計画されたメンテナンス ウィンドウに関するよくある質問に対する回答を示します。
author: angelmarshall
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 6154
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b47ec93f548ed1c7d50480fcb2d2ff2e52837c8d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748123"
---
# <a name="planned-maintenance-window-faq"></a>予定された保守ウィンドウのよく寄せられる質問
[!include [banner](../includes/banner.md)]

### <a name="what-is-a-planned-maintenance-window"></a>計画されているメンテナンス期間とは何ですか ?
メンテナンス予定期間は、機器設備や [サービス](../../fin-ops/get-started/one-version.md) に関する重要な更新を適用するために Microsoft がスケジュール設定をした時間枠です。

### <a name="how-does-a-planned-maintenance-window-work"></a>計画されているメンテナンス ウィンドウはどのように機能しますか。
レベル 2 からレベル 5 のサンドボックス環境および実稼働環境でスケジュールされた計画的保守については、パッチ適用を開始する **5 日前** に Microsoft がすべての利害関係者に通知を送信します。 パッチ適用枠は環境にパッチが適用される期間です。 それは地理的な地域によって定義されます。 保守活動に関する詳細は、関係者に送信される通知に含まれます。 Microsoft が管理するレベル 1 の環境では、更新前に通知は送信されません。 

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
別のよく寄せられる質問 (FAQ) に Microsoft によって行われるサービス更新プログラムに関する詳細が記載されています。 [1 つのバージョンのサービス更新プログラムに関してよく寄せられる質問](../../fin-ops/get-started/one-version.md) を参照してください。

## <a name="infrastructure-updates"></a>機器設備の更新 

### <a name="how-long-is-the-maintenance-window"></a>メンテナンス ウィンドウの長さはどの程度ですか。
ほとんどのオペレーティング システム レベルの更新は約 1 時間で完了します。 ただし、障害を処理してシステムを正常な状態に戻す時間があるため、Microsoft は 3 時間の時間枠を要求しています。 

すべてのアップデートの正確なダウンタイムは、アップデート開始前に通知されるメンテナンス ウィンドウ通知電子メールに含まれます。

### <a name="how-frequent-are-the-updates"></a>更新の頻度を選択してください。
オペレーティング システムレベルの更新は、Microsoft が管理するレベル 2 からレベル 5 のサンドボックス環境と実稼働環境に毎月適用されます。 ただし、Microsoft が管理するレベル 1 環境は、地域ごとに定義されたメンテナンス期間に毎週更新されます。

### <a name="where-can-i-learn-more-about-what-is-applied"></a>何が適用されたかについての詳細はどこですか。
適用される更新プログラムの詳細については、[Microsoft セキュリティ速報](https://technet.microsoft.com/security/bulletins.aspx) を参照してください。

### <a name="where-can-i-track-progress-of-the-update"></a>更新プログラムの進捗はどのように追跡できますか。
オペレーティング システム レベルの更新中に、LCS は現在どのパッチ適用が進行中であるかを示しません。 ただし、Microsoft はこの機能をある時点で追加する予定です。

### <a name="what-environments-are-updated"></a>なんの環境が更新されるか。
オペレーティング システム レベルの更新は、Microsoft の基本サービスの一部として含まれているすべての Microsoft が管理する環境に適用されます。 これには、レベル 1、レベル 2 からレベル 5、および実稼働環境が含まれます。 購入済のアドオンにも適用されます。 ただし、サブスクリプションでホストされている他の環境 (クラウド ホスト環境など) は、顧客またはパートナーが責任を負います。

### <a name="what-notifications-will-i-receive-about-upcoming-planned-maintenance"></a>次回の計画済みメンテナンスに関してどのような通知を受け取りますか ?
更新が予定されている 5 日前に、レベル 2 からレベル 5 のサンドボックス環境および実稼動環境でスケジュールされた更新の通知電子メールが届きます。 この電子メールには、更新される環境、更新の種類、更新が実行する見積もり時間、および実行する必要のある操作に関する情報が含まれます。 Microsoft が管理するレベル 1 環境の通知は送信されません。 

### <a name="will-i-be-notified-when-the-update-is-completed"></a>更新プログラムの完了時に通知されますか。
定義された保守時間枠で更新が完了する場合、更新が完了したときに通知を受信しません。 

### <a name="how-do-i-report-an-issue-that-is-identified-during-validation-of-the-updates-that-were-applied-to-the-environment"></a>環境に適用された更新の検証時に識別される問題をレポートするにはどうすればよいですか。
更新の検証中に特定された問題を報告するには、Microsoft にサポート チケットを提出し、タイトルに '予定された保守時間枠' を追加します。

### <a name="what-happens-if-the-patching-fails"></a>ファイルの修正に失敗した場合はどうなるでしょうか ?
修正が、オペレーティング システム レベル更新中に失敗すると、特定の修正プログラムはスキップされ、次の更新サイクルで適用されます。

### <a name="will-i-be-compensated-if-the-update-takes-longer-than-the-scheduled-maintenance-window"></a>更新プログラムが予定メンテナンス ウインドウより時間がかかる場合は補償されますか。
更新が予定された保守ウィンドウよりも長い場合は、余分な時間は予定外のダウンタイムと見なされ、一般的なサービス レベル アグリーメント (SLA) の対象となります。

### <a name="how-do-i-reschedule-security-maintenance-activities"></a>セキュリティ管理活動を再スケジュールする方法
セキュリティ メンテナンスは、安全な環境の確保するのに役立ちます。メンテナンスを行わないと、回避可能なセキュリティ リスクを招く可能性があります。 

絶対的なビジネス ニーズがあり、上記の期間中にこのメンテナンスを行うことができない場合は、Microsoft にサポート チケットを提出することにより、第 2 層から第 5 層のサンドボックス環境と実稼働環境の現在のメンテナンス活動の再スケジュールを要求できます。 再スケジュール要求をするサポート チケットの提出期限は、通知メールに記載されています。 どんな要求も、締め切りを過ぎて送信された場合には受け付けられません。 

Microsoft が管理する第 1 層の環境では、セキュリティ管理活動を再スケジューリングすることはできません。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
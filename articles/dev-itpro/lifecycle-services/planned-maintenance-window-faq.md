---
title: "予定された保守ウィンドウのよく寄せられる質問"
description: "このトピックでは、Microsoft の計画されたメンテナンス ウィンドウに関するよくある質問に対する回答を示します。"
author: robadawy
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 6154
ms.assetid: 
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: b1ac00edc0c519d4639ad53190148ec94b1780e7
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="what-is-a-planned-maintenance-window"></a>計画されているメンテナンス期間とは何ですか ?

[!include [banner](../includes/banner.md)]

予定された保守ウィンドウは、重要な更新プログラムをクラウド サービスに適用するために Microsoft によってスケジュールされた時間枠です。

### <a name="how-does-a-planned-maintenance-window-work"></a>計画されているメンテナンス ウィンドウはどのように機能しますか。
すべての計画更新については、ウィンドウのパッチ適用を開始する 5 日前に、Microsoft はすべての利害関係者に通知を送信します。 環境に修正プログラムが適用されるときに、または更新プログラムが適用されるときに、地域ごとに定義される修正期間。

プラットフォームの更新中、Microsoft Dynamics Lifecycle Services (LCS) は環境の状態を常に反映し、プロセスに関する電子メールの更新を提供します。 環境ウィンドウの [履歴] セクションには、完了した更新プログラムが表示されます。

現時点では、工程のシステム レベルの更新中に、LCS はパッチ適用中であることを示していません。 この機能を将来のいずれかの時点で追加する予定です。

### <a name="when-is-this-planned-maintenance-window-taken"></a>この計画済みメンテナンス ウィンドウはいつ使用されますか ?
ユーザーへの影響を制限するため、環境が配置されている地域に応じてメンテナンス ウィンドウが予定されています。 次のリストは、各地域のメンテナンス ウィンドウを示しています。 時間は協定世界時 (UTC、グリニッジ標準時) で表示されます。
- NAM: 午前 2:00 から午前 10:00
- SAM: 12 AM から 8 AM
- EMEA: 午後 10 時から午前 6 時
- CAN: 午前 2:00 から午前 10:00
- APAC: 午後 12:00 から午後 3:00

### <a name="what-updates-are-applied-in-the-planned-maintenance-window"></a>計画済みメンテナンス期間に適用される更新
計画メンテナンス ウィンドウ中に、作業システム レベルの更新プログラムおよび重要なセキュリティと信頼性のプラットフォーム更新プログラムが適用されます。 適用される更新プログラムの詳細については、[Microsoft セキュリティ速報](https://technet.microsoft.com/en-us/security/bulletins.aspx) を参照してください。  

### <a name="how-long-is-the-maintenance-window"></a>メンテナンス ウィンドウの長さはどの程度ですか。
オペレーティング システム レベルの更新は、約 1 時間で完了します。

プラットフォーム更新プログラムは、通常、1 ～ 3時間で完了します。 まれに、プラットフォーム更新が完了するまで 8 時間かかる場合があります。

すべてのアップデートの正確なダウンタイムは、アップデート開始前に通知されるメンテナンス ウィンドウ通知電子メールに含まれます。

### <a name="what-environments-are-updated-as-a-part-of-the-planned-maintenance"></a>計画済みメンテナンスの一環として、どのような環境が更新されますか。
プラットフォーム更新プログラムは、Microsoft 基本サービスに含まれるレベル 2 サンドボックス環境に適用されます。 環境が正常にパッチ適用されたことを検証した後、Microsoft はこの更新プログラムを実稼動環境で 5 日間以内に適用します。

オペレーティング システム レベルの更新は、Microsoft の基本サービスの一部として含まれているすべての第 2 層のサンド ボックス環境に適用されます。 購入したアドオンにも適用されます。

第 1 層サンドボックスおよびデモ環境など、他のすべての環境は顧客やパートナーの担当であることに注意してください。

### <a name="what-notifications-will-i-receive-about-upcoming-planned-maintenance"></a>次回の計画済みメンテナンスに関してどのような通知を受け取りますか ?
更新が予定されている 5 日前に、電子メール通知を受け取ります。 この通知には、更新される環境、更新の種類、更新が実行する見積もり時間、および実行する必要のある操作に関する情報が含まれます。

今後、他の通知タイプの有効化を予定しています。
- 電子メール通知 – 計画されたメンテナンス期間の 5 日前に、電子メールの通知が送信されます。 メンテナンスまでの日数、追加の電子メールが送信されます (T-5、T-3、T-1 日)、
- LCS の通知 – LCS の環境の詳細では、次回の更新を選択して今後のメンテナンス ウィンドウのエントリを表示できます。 また、保守ウィンドウの 24 時間前に、リマインダーとして環境にメッセージ バーが表示されます。
- 製品ベースの通知 - Finance and Operations では、システムの予定されたダウンタイムの 2 時間前に、計画的なダウンタイム期間中はシステムを利用できないことをユーザーに知らせる通知が送信されます。

### <a name="who-will-be-notified-about-the-upcoming-planned-maintenance"></a>将来の計画的なメンテナンスはだれに通知されますか。
次の利害関係者には、今後のメンテナンスについて通知されます。
- プロジェクト所有者
- 組織の管理者
- 環境管理者
- 配置の際に、または環境の詳細ウィンドウの [通知] ボタンをクリックして、一覧で指定されたその他の人

### <a name="what-validation-requirements-do-i-have-to-complete"></a>完了する必要のある検証要件とは
プラットフォーム更新プログラムが適用されたとき、検証を実行する必要はありません。 Microsoft は更新に下位互換性および上位互換性があることの保証について責任を負います。 ただし、Microsoft は更新プログラムの適用後にはそれらの検証を実行しないため、必要に応じて、機能の検証を完了できます。 機能の検証を自動化して検証作業を軽減することをお勧めします。

### <a name="what-validations-does-microsoft-do-for-changes-that-will-be-applied-during-the-update"></a>更新時に適用される変更に対する Microsoft の検証とは
更新プログラムが適用される前に、Microsoft は Management reporter または Retail などのプラットフォーム外のコンポーネントに影響がないことを確認する検証を実行します。 また、Microsoft は変更に下位互換性および上位互換性があることを保証します。

更新プログラムが適用されると、Microsoft は正常に完了した事、および環境が予期したとおりに動作している事を検証します。 この検証の一環として、Microsoft はトランザクションを完了するために使用できる Microsoft Dynamics 365 for Finance and Operations を確認するいくつかの基本的な検証テストを実行します。

### <a name="can-i-reschedule-the-planned-maintenance"></a>計画的なメンテナンスを再スケジューリングできますか。
計画的なメンテナンスを再スケジューリングするためのオプションは提供していません。 ただし、現在の月の保守サイクルから除外するように選択できます。 LCS を使用して更新のスケジュールを直接変更できるようにするために、LCS にこのオプションを追加する予定です。 

### <a name="how-do-i-opt-out-of-the-the-current-maintenance-cycle"></a>現在のメンテナンス サイクルを停止するにはどうすればよいですか。
現在のメンテナンス サイクルを無効にするには、Microsoft にサポート チケットを提出してください。 ご使用の環境は、今月の保守サイクルから除外されます。 ただし、お客様の環境は翌月に更新されます。

### <a name="how-do-i-report-an-issue-that-is-identified-during-validation-of-the-updates-that-were-applied-to-the-environment"></a>環境に適用された更新の検証時に識別される問題をレポートするにはどうすればよいですか。
更新の検証中に特定された問題を報告するには、Microsoft にサポート チケットを提出し、タイトルに「計画メンテナンス ウィンドウ」を追加します。

### <a name="what-happens-if-the-patching-fails"></a>ファイルの修正に失敗した場合はどうなるでしょうか ?
プラットフォームの更新のパッチ適用に障害が発生したり、指定された保守時間よりも長く時間がかかった場合、通知はサービス ヘルス ダッシュ ボードに転記されます。 この問題は最優先事項とみなされ、製品チームはそれに対処するようになります。 ただし、簡易修正がない場合、Microsoft は更新プログラムをロールバックし、環境をできるだけ早く正常な状態に戻すことができます。

修正が、オペレーティング システム レベル更新中に失敗すると、特定の修正プログラムはスキップされ、次の更新サイクルで適用されます。

### <a name="will-i-be-notified-when-the-update-is-completed"></a>更新プログラムの完了時に通知されますか。
定義された保守ウィンドウ内で更新が完了する場合、更新が完了したときに通知を受信しません。 ただし、LCS で履歴ページが更新され、更新が完了したことが表示されます。

ダウンタイム ウィンドウの完了時に顧客に通知する機能を追加する予定です。

### <a name="will-i-be-compensated-if-the-update-takes-longer-than-the-scheduled-maintenance-window"></a>更新プログラムが予定メンテナンス ウインドウより時間がかかる場合は補償されますか。
更新が予定された保守ウィンドウよりも長い場合は、余分な時間は予定外のダウンタイムと見なされ、一般的なサービス レベル アグリーメント (SLA) の対象となります。

### <a name="who-is-responsible-for-managing-non-production-environments"></a>だれが非実稼働環境の管理を担当者しますか。
Microsoft 基本サービスに含まれる 第 2 層サンドボックス環境以外では、顧客やパートナーが非製造環境にパッチ適用するための責任者です。 Microsoft が適用したのと同じ更新プログラムを LCS のグローバル アセット ライブラリから取得することができます。 パッケージ名、詳細、および日付情報が電子メール通知に含まれます。

顧客およびパートナーは、すべてのレベル 1 環境でオペレーティング システム レベルの更新を適用する責任があります。

### <a name="will-the-update-from-microsoft-require-any-uptake"></a>Microsoft からの更新プログラムでは何かを取得することが必要ですか。
更新のほとんどにおいて、ユーザーからの取得は不要です。 取得が必要な重要なセキュリティ更新プログラムがある場合は、通知されます。

### <a name="how-do-i-sign-up-to-be-notified-about-the-maintenance-window"></a>メンテナンス ウィンドウに関して通知を受け取るよう登録するにはどうすればよいですか。
パートナー、独立系ソフトウェア ベンダー (Isv)、およびその他の関係者は、将来の特定の更新プログラムを通知する場合、これら 2　つのオプションがあります。

- サービスの状態を確認します。
- 関連する利害関係者 (プロジェクト所有者、環境管理者またはその他の利害関係者) として LCS プロジェクトに追加するよう依頼します。

### <a name="why-cant-these-updates-be-applied-in-zero-downtime"></a>これらの更新プログラムがゼロ ダウンタイムで適用できないのはなぜですか。
サービスのためのダウンタイムの必要性を減らすようたえず努力しています。多くの定期的な保守作業によるダウンタイムは発生しません。 予測可能性を保証するために、ダウンタイムなしですべてのパッチを実行することはまだできません。

### <a name="how-can-i-update-my-environments-with-the-package-from-microsoft"></a>Microsoft からのパッケージで環境を更新する方法はありますか。
Microsoft からのすべてのプラットフォーム 更新パッケージは、グローバル アセット ライブラリの展開可能パッケージ タブで使用できます。 パッケージ名、詳細、および日付情報は、Microsoft から送信される電子メール通知にも含まれています。

階層 1 の環境で Windows 更新プログラムを有効にすることにより、オペレーティング システム レベルの更新プログラムを適用することができます。 その他のすべての環境は Microsoft によって更新されます。

### <a name="because-patching-of-the-production-environment-doesnt-occur-until-five-days-after-patching-of-the-sandbox-environment-for-a-platform-update-how-do-i-make-sure-that-all-the-environments-are-in-the-same-state-and-have-the-same-version"></a>実稼動環境のパッチ適用は、プラットフォーム更新プログラムのためのサンドボックス環境のパッチ適用 5 日後までは発生しないため、すべての環境が同じ状態にあり、同じバージョンであることをどのように確認できるでしょうか。
Microsoft は、第 2 層のサンドボックス (実稼働前) 環境で更新を適用します。 その更新が成功した場合は、Microsoft は実稼動環境にそれを適用します。 実稼働環境の更新の通知は、更新の 5 日前に送信されます。

Tier-2 サンドボックスと実稼働環境のバージョンが 5 日間異なることを希望しない場合は、Dynamics サービス エンジニアリング (DSE) チームにサービス リクエストを送信して、通常の生産更新フローを通してパッケージを適用し、実稼働環境を更新できます。 (パッケージは、グローバル アセット ライブラリで利用可能です。)

サンドボックス環境と製品環境のバージョンに違いがあっても、その製品を引き続き使用できます。 ただし、サンドボックス環境と本番環境が同じバージョンになるまで、パッケージを本番環境に移動したり、真の検証を完了することはできません。

### <a name="is-there-a-way-to-roll-back-a-package-that-microsoft-applied"></a>Microsoft が適用したパッケージをロールバックする方法はありますか。
現在、Microsoft が適用したパッケージをロールバックする方法はありません。

### <a name="how-are-batch-jobs-handled-as-part-of-this-maintenance"></a>このメンテナンスの一環としてバッチ ジョブはどのように処理されますか。
バッチ ジョブはメンテナンス ウィンドウ中に中断され、メンテナンスの完了時に再開します。

### <a name="where-can-i-check-that-the-update-was-completed-successfully"></a>更新プログラムが正常に完了したことを確認する場所は?
更新プログラムが LCS の履歴ページで正常に完了したことを確認することができます。 そこに、Microsoft が計画したメンテナンス期間 - 完了のエントリが表示されます。

### <a name="where-can-i-see-which-updates-are-included-in-the-package-that-is-being-applied"></a>適用されるパッケージに含まれている更新プログラムをどこで確認できるか
グローバル アセット ライブラリの説明列は、パッケージの内容を示します。



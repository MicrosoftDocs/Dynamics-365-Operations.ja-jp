---
title: "Finance and Operations クラウド プラットフォームの毎月の更新プログラムのよく寄せられる質問"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations クラウド プラットフォームの毎月の更新に関する重要な情報を提供します。"
author: manalidongre
manager: AnnBe
ms.date: 05/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 273383
ms.assetid: ac5c9f89-98a6-481f-a0d6-a9627e01030e
ms.search.region: Global
ms.author: meeram
ms.dyn365.ops.version: Platform update 5
ms.search.validFrom: 2017-03-31
ms.translationtype: HT
ms.sourcegitcommit: 62dbf8ffd550f9369df1ac8399b25c76f3d57c93
ms.openlocfilehash: 1f6f507ae921b2a39248efa2d8196e0f31926405
ms.contentlocale: ja-jp
ms.lasthandoff: 07/03/2018

---

# <a name="finance-and-operations-cloud-platform-monthly-updates-faq"></a>Finance and Operations クラウド プラットフォームの毎月の更新プログラムのよく寄せられる質問

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations クラウド プラットフォームの毎月の更新に関する重要な情報を提供します。

## <a name="what-is-the-rationale-behind-the-cloud-platform-monthly-updates"></a>クラウド プラットフォームの月次更新の論理的根拠は何ですか ?

Platform update 3 以降、Microsoft は Finance and Operations のクラウド プラットフォームで後方互換性を維持するよう努めており、プラットフォームに煩雑なカスタマイズを加える機能を削除しました。 (そのカスタマイズの方法は、*オーバーレイ*とも呼ばれます。) さらに、プラットフォームの更新プログラムはカスタムコードに対してバイナリと互換性があるため、プラットフォーム更新プログラムを行うためにコードをコンパイルする必要はありません。 したがって、拡張機能を使用する豊富なカスタマイズを行うことができますが、コストのかかるコードのアップグレードを行わずに、最新の状態を維持できます。

Platform update 4 以降、クラウド プラットフォームの毎月の更新プログラムがリリースされています。 したがって、ボタンをクリックするだけで、最新のイノベーションを使って新しい環境や既存の環境を最新の状態に保つことができます。 毎月のプラットフォーム更新プログラムには互換性があり、既存の機能の動作を変更する機能について明示的なオプトイン オプションが追加されます。

## <a name="why-do-i-have-to-move-to-the-latest-platform-update"></a>最新のプラットフォーム更新プログラムに移動する必要があるのはなぜですか。

最新のリリース済プラットフォーム バージョンへの移行によって、全体の信頼性とサービス エクスペリエンスを向上させ、環境に存在する既知の問題を修正できます。 したがって、Microsoft がリリースした最新のプラットフォーム更新プログラムを最新の状態にする必要があります。

## <a name="is-this-a-one-time-activity-or-will-future-platforms-also-be-pushed-in-a-similar-manner"></a>これは 1 回限りのアクティビティですか、それとも今後のプラットフォームでも同様の方法が求められますか。

[ソフトウェアのライフサイクル ポリシー](../migration-upgrade/versions-update-policy.md) にあるように、Microsoft は環境が更新され、最新のものであることを保証するために引き続きお客様と密接に協力していきます。 2018 年 7 月以降は、すべての顧客環境が継続的に更新され、最新バージョンが常に反映されます。 これらの変更の詳細については、[ソフトウェアのライフ サイクル ポリシー](../migration-upgrade/versions-update-policy.md) を参照してください。

## <a name="what-kind-of-update-will-be-applied"></a>どのような種類の更新が適用されますか ?

プラットフォーム更新プログラム パッケージがユーザーの環境に適用されます。 このパッケージは、プラットフォームに加えられた新機能とバイナリ修正のコレクションです。 このパッケージには、アプリケーション (X++ またはバイナリ) の修正は含まれていません。

## <a name="what-is-the-overall-process-that-will-be-used"></a>使用される全体的なプロセスはどのようになっていますか ?

Microsoft は、購入したレベル 2 スタンダード承認テスト (サンドボックス) 環境に更新プログラムが適用される 5 日前に通知します。 更新プログラムを実稼働環境に適用する前に、5 日間で、サンド ボックス環境でプラットフォーム バージョンをテストして検証します。 明示的なサインオフは必要ありません。

## <a name="what-is-the-expected-downtime"></a>予想されるダウンタイムはどのくらいですか ?

更新が正常に完了するために予想されるダウンタイムは 1 時間です。 ただし、 更新プログラムの適用時に問題が発生する場合、3 時間のダウンタイムを要求します。 マイクロソフトは、必要とするダウンタイムを減らすために積極的に取り組んでいます。改善は将来のリリースに反映されます。

## <a name="where-can-i-find-details-about-the-maintenance-windows-when-the-update-will-be-applied"></a>更新プログラムが適用されるときのメンテナンス ウィンドウの詳細はどこに記述されていますか ?

電子メール通知には更新される環境、ダウンタイムの金額、および更新が適用される時間に関する詳細が含まれます。 詳細については、[計画済みメンテナンス ウィンドウとは何ですか](../lifecycle-services/planned-maintenance-window-faq.md) を参照してください

## <a name="who-will-receive-the-email-notifications"></a>電子メール通知はだれが受け取りますか。

Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトの所有者、組織の管理者、および環境マネージャー ロールは、電子メール通知を受け取ります。 プロジェクトの一部ではなく通知を受けたい場合は、特定の環境の環境詳細ページの通知リストで、関心のあるステーク ホルダーの電子メール アドレスをコロン区切りのリストとして追加します。 今後、これからの更新スケジュールの公開を検討しています。

## <a name="do-i-have-to-do-anything-to-prepare-for-the-update"></a>更新プログラムの準備に何か実行する必要があるか。

お客様は購入したレベル 2 スタンダード承認テスト (サンドボックス) 環境と実稼働環境での完全なパッケージ アプリケーションに署名することだけが求められます。 サインオフするには、環境の詳細ページで、パッケージ アプリケーションの状態を **サインオフ** に設定します。

## <a name="what-details-will-the-release-notes-for-platform-updates-provide-will-there-be-a-list-of-fixes-and-new-features-and-information-about-the-processes-that-those-fixes-and-features-affect"></a>プラットフォームの更新プログラムのリリース ノートが提供する詳細情報とは 修正および新機能の一覧、およびそれらの修正や機能が影響を与えるプロセスに関する情報の一覧はありますか。

最新の月次更新プログラムの新機能や変更された機能の一覧は、[[新機能または変更点](../../fin-and-ops/get-started/whats-new-changed.md)] を参照してください。 新しい修正プログラムと機能を記述した Microsoft サポート技術情報 (KB) 記事も公開します。 現在公開されている、[新機能および変更された機能](../../fin-and-ops/get-started/whats-new-changed.md) トピックに対して提供されるフィードバックは、通信にギャップがあるかどうかを把握するのを助けます。 

プラットフォーム更新プログラムには、アプリケーションの変更が含まれていません。 したがって、影響は最小限に抑える必要があります。

## <a name="what-validations-does-microsoft-do-for-platform-changes-that-will-be-applied-during-the-update"></a>更新時に適用されるプラットフォームの変更に対する Microsoft の検証とは

更新プログラムが適用される前に、Microsoft は Management reporter および Retail などのプラットフォーム外のコンポーネントに影響がないことを確認する検証を実行します。 また、Microsoft は変更に下位互換性があることを保証します。

更新プログラムが適用されると、Microsoft は正常に完了した事、および環境が予期したとおりに動作している事を検証します。 この検証の一環として、Microsoft はトランザクションを完了するために使用できる Finance and Operations を確認する検証テストを実行します。

## <a name="what-kind-of-validation-requirements-do-i-have-to-complete"></a>どのような種類の検証要件を完了する必要がありますか ?

プラットフォーム更新プログラムが適用されたとき、検証を実行する必要はありません。 Microsoft は更新に標準の Finance and Operations との下位互換性があることの保証について責任を負います。 ただし、Microsoft は更新プログラムの適用後にはこれらの検証を実行しないため、必要に応じて、重要なシナリオの基本的な受け入れテストを完了できます。 たとえば、プラットフォーム コンポーネントには Microsoft Office および Microsoft Excel 統合、ワークフロー、フォームの個人用設定、データ管理フレームワーク、ODATA 統合、エンティティ ストア、および Microsoft Power BI 統合が含まれます。 これらのコンポーネントが含まれる機能をテストすることが有益であることがわかる場合があります。

機能の検証を自動化して検証作業を軽減することをお勧めします。

## <a name="what-tools-does-microsoft-provide-to-manage-and-run-acceptance-tests"></a>受け入れテストの管理と実行に Microsoft が提供するツールは何ですか ?

[継続的な配信ホーム ページ](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/dev-tools/continuous-delivery-home-page)と [AX 7 の自動テスト ガイダンス](https://blogs.msdn.microsoft.com/axdevalm/2016/08/12/automated-testing-guidance-for-ax-7/)のブログ記事を参照してください。

## <a name="what-are-the-timeframes-how-long-will-i-have-to-validate"></a>時間枠とは どのくらいの期間検証する必要がありますか。

5 営業日で、サンド ボックスと実稼働更新プログラム間の環境を検証します。

## <a name="how-do-i-report-an-issue-that-is-identified-during-validation-of-the-update-that-was-applied-to-the-environment"></a>環境に適用された更新の検証時に識別される問題をレポートするにはどうすればよいですか。

LCS 経由で既存のサポート チャンネルから問題を報告する必要があります。

## <a name="what-is-the-process-if-i-find-issues-in-the-sandbox-environment"></a>サンド ボックス環境で問題が見つかった場合のプロセスはどうなりますか ?

サンド ボックス環境に問題がある場合は、op-out 調査を完了し更新を延期することができます。 その更新を最大 30 日間延期することができます。 この場合、Microsoft が調べられるように、検出された問題のサポート インシデントを記録する必要があります。

## <a name="how-can-i-revert-a-platform-update-if-i-find-an-issue-during-validation"></a>検証中に問題を見つけた場合に、プラットフォーム更新プログラムを戻す方法がありますか。

現在、正常に行われた更新をロールバックすることはできません。 ただし、数か月後には、プラットフォーム更新プログラムをロールバックする方法が提供されます。

## <a name="are-management-reporter-retail-and-document-routing-agent-updated"></a>Management Reporter、Retail、ドキュメント回覧エージェントは更新されていますか。

Management reporter および Retail は、Microsoft がリリースするプラットフォーム更新プログラムに含まれません。 ただし、2018 年 5 月以降、財務報告は更新に含められます。

ドキュメント回覧エージェントの更新は、顧客によって管理されるものであり、プラットフォーム更新プログラムの一部ではありません。

## <a name="are-batch-jobs-and-external-pieces-suspended-how-is-this-process-managed"></a>バッチ ジョブと外部ピースを中断していますか。 このプロセスはどのように管理されますか。

バッチ ジョブはメンテナンス ウィンドウ中に中断され、メンテナンスの完了時に再開します。

## <a name="how-long-can-i-stay-on-a-specific-monthly-platform-update"></a>特定の毎月のプラットフォーム更新プログラムにはどのくらいの期間とどまれますか。

[ソフトウェア ライフサイクル ポリシー](../migration-upgrade/versions-update-policy.md)は、マイクロソフトからリリースされる最新のプラットフォーム更新を顧客が導入する必要があることを示しています。 更新を最大 30 日間延期することができます。 その後は、環境が更新されます。 詳細については、[ソフトウェアのライフ サイクル ポリシー](../migration-upgrade/versions-update-policy.md) を参照してください。

## <a name="how-can-i-get-early-access-to-the-platform-bits-for-validation"></a>検証用プラットフォーム ビットへの早期アクセスをどのように取得できますか。

ユーザーがパートナーであり、プラットフォームのアップデートに早期にアクセスすることに興味がある場合は、<http://aka.ms/PEAPnomination> での推薦アンケートを送信することで、[PEAP プログラム](http://aka.ms/PEAPnomination)に参加します。 ユーザーが顧客であり、常に最新のプラットフォームで環境を稼働させたい場合は、<http://aka.ms/CAAPnomination> の推薦アンケートを送信します。

## <a name="how-can-i-get-the-exact-package-version-that-is-applied-to-my-sandbox-environment-by-microsoft-"></a>Microsoft のサンドボックス環境に適用される正確なパッケージ バージョンを取得する方法は？

Microsoft がレベル 2 サンドボックス環境を更新すると、パッケージ バージョンのコピーが LCS プロジェクト アセット ライブラリに保存されます。

## <a name="i-prefer-that-microsoft-update-a-standard-acceptance-test-sandbox-environment-that-differs-from-the-tier-2-sandbox-environment-that-i-purchased-what-can-i-do"></a>購入した階層 2 サンドボックス環境とは異なる、Microsoft 更新プログラム Standard Acceptance Test (Sandbox) 環境を希望します。 実行できることは何ですか ?

オプトアウト調査で、Microsoft は異なるサンドボックス環境 ID を入力できる場所を提供します。 Microsoft は第 1 層サンドボックス環境を更新しないことに注意してください。 第 1 層のサンド ボックス環境は、単一の仮想マシン (VM) として展開される環境です。

## <a name="can-i-opt-in-to-have-microsoft-manage-additional-environments"></a>Microsoft が追加の環境を管理することにオプトインすることができますか。

現在、更新される環境のみが既定のレベル 2 スタンダード承認テスト (サンドボックス) 環境です。 ただし、顧客が追加のレベル 2+ 環境をオプトインする方法を提供します。

## <a name="what-if-the-timeframe-that-is-proposed-doesnt-work-with-my-schedule-or-i-want-a-different-window-for-the-update"></a>提案された時間枠が自分のスケジュールと合わない場合、または更新プログラムに別のウィンドウを望む場合はどうしますか ?

電子メールの通信には、オプトアウト調査へのリンクが含まれています。 この調査では、別の日付を選択できます。 ただし、最大 30 日間更新を延期することができます。

## <a name="will-the-updates-be-forced-every-month-or-will-there-be-some-allowance-to-delay-the-updates"></a>更新プログラムは毎月強制されますか。それとも更新プログラムを延期することができますか。

お客様が時流に乗り遅れないようにする必要があります。 顧客は最大30日まで更新を遅らせることができます。 その後、プラットフォームの最新のリリースでは、環境が更新されます。

## <a name="when-should-i-update-my-devbuild-environment"></a>自分の開発/ビルド環境をいつ更新すればよいでしょうか ?

Microsoft が実稼働環境を更新した後、更新プログラムを残りの環境 (追加のサンドボックスと開発/ビルド環境など) に適用されます。 LCS の環境詳細ページで、**プラットフォーム更新** タイルから最新のプラットフォーム更新パッケージを取得することができます。 詳細については、[最新のプラットフォーム更新プログラムの環境への適用](../migration-upgrade/upgrade-latest-platform-update.md) を参照してください。

## <a name="in-the-scenario-where-microsoft-initiates-platform-updates-if-an-update-is-completed-on-a-tier-2-standard-acceptance-test-sandbox-environment-but-isnt-yet-applied-to-the-production-environment-there-is-a-gap-of-five-days-when-the-sandbox-and-production-environments-are-on-different-versions-if-we-find-an-issue-in-the-production-environment-can-we-still-follow-the-process-of-applying-a-package-to-the-sandbox-environment-and-then-moving-it-to-the-production-environment-even-though-the-versions-the-environments-are-on-different-versions"></a>Microsoft がプラットフォーム更新プログラムを開始するシナリオで、レベル 2 スタンダード承認テスト (サンドボックス) 環境で更新を完了したが、実稼働環境にまだ適用されていない場合、5 日間サンドボックス環境と実稼働環境が異なるバージョンになります。 実稼動環境で問題が見つかった場合、環境が異なるバージョンであっても、サンドボックス環境にパッケージを適用してから運用環境に移行するプロセスには引き続き対応できますか?

はい。 プラットフォーム更新プログラムは下位互換性があるため、レベル 2: スタンダード承認テスト (Sandbox) と実稼動環境が異なるバージョンであっても、まずパッケージをサンドボックス環境に適用してから実稼動環境に移動することができます。 このフローはサポートされています。 また、実稼働環境のプラットフォームを既定の階層 2 スタンダード承認テスト (サンドボックス) 環境のプラットフォームと同じバージョンに積極的に更新することができます。 

## <a name="how-can-i-get-early-access-to-non-released-platform-updates"></a>非リリースのプラットフォーム更新プログラムへの早期アクセスをどのように取得できますか。

Microsoft Continuous Auto-Update Advantage Program (CAAP) に参加することができます。ここでは Microsoft がユーザーのプラットフォームを常に最新に保ちます。 プログラムの詳細情報やサインアップについては、<http://aka.ms/CAAPnomination> から推薦アンケートを検索できます。

## <a name="we-have-seen-cases-where-isv-solutions-are-dependent-on-platform-updates-how-can-we-make-sure-that-versions-that-are-compatible-with-the-platform-update-are-available-from-all-involved-isvs-before-the-platform-update-is-applied"></a>ISV ソリューションがプラットフォームの更新プログラムに依存する事例が確認されました。 プラットフォーム更新プログラムが適用される前に、プラットフォーム更新プログラムと互換性のあるバージョンが ISV を含むすべてから利用可能であることをどのように確認できますか。

独立系ソフトウェア ベンダー (ISV) は、そのコードに応じる最低限必要なプラットフォーム リリースで開発します。 お客様の環境のプラットフォーム更新プログラムは互換性のあるものになります。 ただし、ISV は、プラットフォーム ビットへの早期アクセスを獲得して、一般的に使用できるようになる前にプラットフォームに対するソリューションを検証できるようにするために、PEAP プログラムの一部とすることをお勧めします。

## <a name="what-level-of-involvement-do-you-foresee-for-the-implementation-partners"></a>実装パートナーに対してどのレベルの関与を予測されますか ?

パートナーは、顧客環境に適用される前にプラットフォーム ビットに早くアクセスできるように、PEAP プログラムに参加することをお勧めします。 唯一の関与は、他の環境も更新されていることを確認することです。 

## <a name="can-partners-see-the-communications-about-platform-updates-before-the-customer-or-can-they-get-an-update-earlier"></a>パートナーが顧客の前にプラットフォーム更新プログラムに関するコミュニケーションを確認する、またはパートナーが早く更新を入手することができますか。

パートナーは、プラットフォーム ビットへの早期アクセスを取得する PEAP プログラムにサインアップすることができます。 また、通知リストを使用してパートナーを顧客のプロジェクトに利害関係者または当事者として追加するように依頼します。 今後の数か月間の更新のスケジュールの公開を検討しています。


---
title: 1 つのバージョンのサービス更新に関するよく寄せられる質問
description: このトピックでは、一貫性があり、予測可能でシームレスな方法で最新の状態に保つために使用できるサービスの更新、プロセス、ツールについて明確に説明します。
author: laneswenka
ms.date: 05/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5f5b65dc05e0269fd7af9b0eb95dc35fc62d595e
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770127"
---
# <a name="one-version-service-updates-faq"></a>1 つのバージョンのサービス更新に関するよく寄せられる質問

[!include[banner](../includes/banner.md)]

このよく寄せられる質問は、変更の準備のために使用できるサービスの更新プログラム、プロセス、ツールを明確にすることを目的としています。 必要に応じて、このトピックに追加情報を追加し続けします。

1 つのバージョンのサービス更新の詳細については、[1 つのバージョンのサービス更新の概要](../../dev-itpro/lifecycle-services/oneversion-overview.md)を参照してください。

### <a name="can-the-updates-be-delayed-what-is-the-policy"></a>更新を遅らせることができますか? ポリシーとは何ですか?

はい、Microsoft Dynamics Lifecycle Services (LCS) プロジェクトの更新設定を使用して、すべてのサンドボックス環境と運用環境が利用可能な最新の更新プログラムより 3 バージョン以内の場合、更新プログラムを一時停止、遅延、またはオプトアウトできます。 顧客は、最大 3 つまでの更新を続けて一時停止することができます。 以下は、遅延更新の例です。 

- 顧客は現在バージョン 10.0.22 を使用しています。
- 顧客は、更新 10.0.23、10.0.24、および 10.0.25 を一時停止できます。
- 顧客は、10.0.26 更新プログラムが利用可能になったら、入手する必要があります。

更新プログラムを一時停止する方法の詳細については、[Lifecycle Services (LCS) によるサービスの更新の一時停止](../../dev-itpro/lifecycle-services/pause-service-updates.md)を参照してください。

### <a name="if-the-release-date-is-in-early-april-when-will-the-general-availability-package-become-available"></a>4 月の始めのリリースで、一般提供パッケージはいつ使用可能になりますか?

リリースの製品更新プログラムは、月の 1、2、3 週間目に予定されています。 LCS でセットアップした構成により、その特定の週に更新プログラムを受け取ります。 サンドボックスの更新プログラムは、常に実稼働更新の 1 週間前にスケジュールされます。 コンフィギュレーション設定は LCS で利用できます。

たとえば、4 月の 10.0.25 リリースの場合、Microsoft は LCS でセットアップした構成によって 4 月 1 日、4 月 8 日、または 4 月 15 日の週末に更新プログラムを実行しました。 サンドボックスの更新プログラムは、常にその更新の 1 週間前にスケジュールされます。

顧客は、LCS で提示されているよりも早い時期、またはより都合のいい時間に更新プログラムを適用することを選択できます。 顧客が最新バージョンを使用している場合、自動更新がキャンセルされます。

## <a name="service-updates"></a>サービスの更新

### <a name="what-product-versions-are-affected-by-service-updates"></a>どの製品バージョンがサービスの更新プログラムの影響を受けますか?

| バージョン       | Description |
|---------------|-------------|
| 8.1 以降 | バージョン 8.1 以降のすべての顧客には、毎月の自動更新プログラムがスケジュールされています。 これらの更新プログラムは、アプリケーションとプラットフォームの更新が組み合わされたものです。 現在の更新プログラムから 3 つ以内の更新プログラムを使用している必要があります。 更新プログラムを一時停止する方法の詳細については、[サービス更新の一時停止](../../dev-itpro/lifecycle-services/pause-service-updates.md)を参照してください。 |

### <a name="what-do-the-service-updates-contain"></a>サービス更新プログラムには何が含まれていますか?

リリース 8.1 以降では、サービスの更新には、規制の更新を含むサービスの重要な改良であるアプリケーション (財務、レポート、小売を含む) とプラットフォームの変更が含められます。 このような変更には、規制の更新が含まれます。 新しいエクスペリエンスは構成可能になります。 サービス更新プログラムには、下位互換性があります。 更新プログラムを表す 1 つのバージョンがあります。

### <a name="what-is-a-regulatory-update"></a>規制の更新とは何ですか?

規制の更新は、法律 (通常は特定の国/地域) によって義務付けられている新機能または既存の機能の変更です。 規制の更新は、特定の法律実施日 (LED) に常に要求され、その日付以前に有効にする必要があります。

### <a name="what-is-the-upcoming-schedule-of-updates"></a>今後の更新スケジュールは?

毎年、7 つのサービス更新がリリースされました。 都合の良いときに更新プログラムを適用したり、選択されたメンテナンス期間に基づいて Microsoft が自動更新を適用するようにしたりするオプションがあります。 現在の更新プログラムから 3 つ以内の更新プログラムを使用している必要があります。

対象となるリリースのスケジュールについては、[サービス更新プログラムの使用可能性](public-preview-releases.md)を参照してください。

### <a name="are-there-any-major-updates-post-81"></a>8.1 以降のメジャー アップデートはありますか?

毎年、4 月更新と 10 月更新の 2 つのメジャー更新プログラムがあります。 これらの更新プログラムによって新しいエクスペリエンスが有効になります。 メジャー更新プログラムでは、コードやデータのアップグレードは必要ありません。 重大な変更はお客様が計画できるように、12 か月前にお知らせします。 重大な変更は、メジャー更新プログラム中にのみ導入されます。

### <a name="what-does-it-mean-when-an-update-is-backward-compatible"></a>更新プログラムに下位互換性がある場合、これは何を意味しますか?

下位互換性では、バイナリと機能の互換性がカバーされます。 バイナリ互換性は、カスタマイズを再コンパイル、再構成、または再展開しなくても、あらゆるランタイム環境に更新プログラムを適用できることを意味します。 これはまた、デザイン時の開発環境で、X++ パブリックおよび保護されたアプリケーション プログラミング インターフェイス (API) とメタデータが変更または削除されないことも意味します。 Microsoft が古い形式の API を削除することによって互換性をなくす必要がある場合、この変更は 12 か月前に通知され、廃止スケジュールに従います。 機能互換性は、ユーザー エクスペリエンスに関するものです。 すべての新しいエクスペリエンスは、12 か月間オプトイン ベースで利用できます。

下位互換性には、非 X++/メタデータ API は含まれていません。 Microsoft は、事前に通知することなく、製品が使用する依存関係を更新し、依存関係を削除する権限を保有します。 Microsoft は、この確約が明記された場合を除いて、依存ソフトウェア ライブラリの下位互換性を維持することを約束しません。 

非推奨のガイドライン、非推奨のメソッドおよびメタデータ要素の詳細については、[メソッドとメタデータの要素の非推奨](../../dev-itpro/migration-upgrade/deprecation-deletion-apis.md)を参照してください。

### <a name="can-i-apply-a-platform-service-update-to-my-existing-81-or-later-environments"></a>プラットフォーム サービスの更新を既存の 8.1 以降の環境に適用することができますか。

バージョン 8.1 以降の顧客は、8.1.x または v10.x のサービス更新プログラムのみ適用することができます。 プラットフォームのみのサービス更新プログラムをバージョン 8.1 以降に適用することはできません。 

### <a name="service-updates-for-on-premises-deployments"></a>オンプレミス配置のためのサービス更新

クラウド配置とオンプレミス配置の両方に対して、ポリシーとサービス更新スケジュールが同じになりました。 たとえば、最大 3 回までの連続した更新プログラムを遅延するオプションは、両方のタイプの配置に適用されます。 これらの更新プログラムをそれぞれ適用するプロセスは、そのまま若干異なります。 詳細については、[オンプレミス配置への更新プログラムの適用](../../dev-itpro/deployment/apply-updates-on-premises.md#update-an-on-premises-deployment)を参照してください。

## <a name="process"></a>処理

### <a name="how-will-microsoft-ensure-the-quality-of-releases"></a>Microsoft はリリースの品質を確保していますか?

リリースの品質を保つことは基本的な原則であり、[サービス更新プログラムの使用可能性](public-preview-releases.md)で説明されている一連の進歩的かつ厳格な自動検証によって可能になっています。

### <a name="can-i-select-the-day-and-time-to-update"></a>更新する日時は選択できますか?

ユーザーは、LCS に日と保守の時間枠を構成できます。 更新プログラムの設定に基づくサービス更新は、15分以内に開始されます。 LCS 通知を受信するようにオプトインしたユーザーには、更新手順が記載された電子メールが届きます。 ユーザーは、更新プログラムの指定された階層 2/UAT サンドボックスを選択できるようになります。 ユーザーは、テストと検証を行うのに 7 カレンダー日あります。

ユーザーは、LCS からのすべての環境に対して、以前の更新プロブラムを適用することもできます。 実稼働準備ができた配置可能パッケージは、LCS のアクション センターを介してすべてのユーザーが入手できます。 追加のすべてのサンドボックスは、運用環境と同じ日に自動更新されます。 詳細については、[サービス更新の構成](../../dev-itpro/lifecycle-services/configure-service-updates.md) を参照してください。

### <a name="a-service-update-was-applied-to-the-environment-in-lcs-what-does-the-number-on-the-tile-for-this-environment-represent"></a>サービス更新プログラムは環境に適用されました。 LCS では、この環境のタイルの番号は何を表していますか?

Microsoft は、すべての顧客に同じサービス更新プロブラムを自動的に適用します。 Microsoft は、引き続き最新の更新プログラムを提供します。 LCS の環境のタイルの番号は、環境に適用できる修正プログラム数の累計を表します。 Microsoft は、すべての顧客に同じバージョンのみ自動適用するため、必要な場合、顧客には累積的な修正プログラム パッケージを適用する責任があります。

### <a name="how-do-i-update-to-the-latest-version"></a>最新バージョンに更新する方法を教えてください。

ユーザーは、LCS の環境の詳細ページでタイルを使用して最新バージョンに更新できます。 Microsoft により更新プログラムがリリースされたら、タイルに更新プログラムが表示されます。 ユーザーは、サンドボックスと製造環境で更新エクスペリエンスを経由して独自に更新プログラムを適用することができます。 

### <a name="how-do-i-update-the-production-environment-to-the-same-version-after-microsoft-updates-the-sandbox-environment"></a>Microsoft がサンドボックス環境を更新した後で、実稼働環境を同じバージョンに更新する方法を教えてください。

Microsoft がサンドボックス環境を更新すると、更新に使用されるパッケージはプロジェクトの資産ライブラリに保存されます。 パッケージ名の先頭には "サービスの更新" という語が付いています。 そのパッケージはすでにサンドボックス環境に適用済みのため、このをリリース候補としてマークできます。 その後で運用環境に移動し、他の更新プログラムを適用するのと同様にパッケージを適用するようスケジュールすることができます。

### <a name="what-is-the-expected-downtime"></a>予想されるダウンタイムはどのくらいですか ?

更新が正常に完了するために予想されるダウンタイムは 1 時間 30 分です。 ただし、 更新プログラムの適用時に問題が発生する場合、3 時間のダウンタイムを要求します。 Microsoft は、必要とするダウンタイムを減らすために積極的に取り組んでおり、改善は数か月以内に反映されます。

### <a name="what-is-the-process-for-deprecation"></a>廃止のプロセスを教えてください。

製品から機能が削除される前に、削除の 12 ヶ月前に製品文書で廃止予定の発表がされます。

互換性を破る変更で、それがコンパイル時間にのみ影響を与えるが、サンドボックスと運用環境に対するバイナリ互換である場合、廃止期間は 12 ヶ月未満になります。 通常、これらの変更は、コンパイラに対して行う必要がある機能更新です。

### <a name="can-i-delay-an-update"></a>更新プログラムを延期することはできますか?

はい、 Lifecycle Services (LCS) プロジェクトの更新設定を使用して、すべてのサンドボックス環境と運用環境が利用可能な最新の更新プログラムより 3 バージョン以内の場合、更新プログラムを一時停止、遅延、またはオプトアウトできます。 この期間後は、更新プログラムがスケジュールされ、Microsoft により自動適用されます。 遅延更新用の更新エクスペリエンスにより、さらなるダウンタイムが発生します。

### <a name="can-i-delay-an-update-for-longer-than-three-consecutive-service-updates-because-of-seasonal-activity-or-another-business-reason"></a>季節的なアクティビティやその他のビジネス上の理由により、連続したサービス更新プログラムを 3 回以上遅らせることはできますか? 

いいえ。 サービス更新プログラムはサンドボックスに自動的に適用されます。 そして 7 日後、環境が 3 サービス更新プログラムより古い場合、更新プログラムがすべての追加のサンドボックスと運用環境に適用されます。 顧客は、最大 3 つの連続した更新のみ連続して一時停止できます。 たとえば、バージョン 10.0.22 の顧客が 10.0.23、10.0.24、10.0.25 の更新プログラムを一時停止する場合、サービス更新プログラム 10.0.26 は、まずサンドボックス環境に適用され、その後、すべての追加のサンドボックスと運用環境に自動的に適用されます。 

### <a name="what-happens-to-an-environment-that-is-running-a-finance-and-operations-app-version-that-is-no-longer-supported"></a>サポートされなくなった財務と運用アプリ バージョンを実行している環境はどうなりますか?

サポートされなくなった財務と運用アプリ バージョンを実行している環境では、LCS の環境の詳細ページの上部に警告メッセージが表示されます。

すべての Microsoft が管理する環境、およびオンプレミス実装プロジェクトのサンドボックス環境と運用環境では、サポートされなくなった財務と運用アプリ バージョンを実行している環境において一部の Lifecycle Services (LCS) 機能を使用できない場合があります。 この機能には、次のアクションを完了する機能が含まれます。

- メンテナンス モードの有効化。
- 環境または環境間でデータベースを移動するために提供されるすべての機能を使用する。
- SQL Server データベースへのファイアウォール アクセスの有効化。
- Regression suite automation tool (RSAT) 証明書のダウンロード。
- RSAT 証明書を再生成する。

サポートされているバージョンにサービス更新を適用すると、この機能は影響を受ける環境で使用できます。

> [!NOTE]
> このトピックでは、バージョンについて次のように記載されています。
>
> - バージョン N は最新バージョン (たとえば、10.0.25)
> - バージョン N-1 は N よりも 1 つ古いバージョン (たとえば、10.0.24)
> - バージョン N-2 は N よりも 2 つ古いバージョン (たとえば、10.0.23)
> - バージョン N-3 は N よりも 3 つ古いバージョン (たとえば、10.0.22)
> - バージョン N-4 は N よりも 4 つ古いバージョン (たとえば、10.0.22) (この例では、バージョン 10.0.21 の顧客は更新を一時停止 **できません**。)

### <a name="how-do-the-automatic-updates-affect-my-microsoft-managed-additional-sandbox-environments-in-my-lcs-implementation-project"></a>自動更新によって、LCS 実装プロジェクトで Microsoft が管理する追加のオブジェクト環境はどのような影響を受けますか? 

追加のすべてのサンドボックス環境は、実稼働環境と同じ更新ウィンドウ内に更新され、生産更新に使用されているのと同じリリース バージョンに更新されます。 この更新は、N-3 ライフサイクル ポリシーでサポートされている追加のサンドボックス環境にも適用されます。 

### <a name="what-if-one-additional-sandbox-environment-is-on-n-1-and-another-is-on-n-4-the-default-sandbox-environment-and-the-production-environment-are-on-less-than-version-n"></a>追加のサンドボックス環境の 1 つが N-1 で、他の環境が N-4 の場合 (既定のサンドボックス環境と実稼働環境がバージョン N より前の場合) はどうなりますか? 

すべての環境がバージョン N に更新されます。 

### <a name="what-if-the-default-sandbox-environment-is-manually-updated-before-the-default-sandbox-environment-email-is-sent"></a>既定のサンドボックス環境の電子メールが送られる前に、既定のサンドボックス環境が手動で更新される場合はどうなりますか? 

既定のサンドボックス環境、実稼働環境の自動更新および追加のすべてのサンドボックス環境はキャンセルされます。

### <a name="what-if-the-default-sandbox-environment-is-manually-updated-after-the-default-sandbox-email-is-sent"></a>既定のサンドボックス環境の電子メールが送られた後に、既定のサンドボックス環境が手動で更新される場合はどうなりますか? 

既定のサンドボックス環境、実稼働環境の自動更新および追加のすべてのサンドボックス環境はキャンセルされます。 

### <a name="what-if-the-production-environment-is-manually-updated-before-the-production-environment-email-is-sent"></a>実稼働環境の電子メールが送られる前に、実稼働環境が手動で更新される場合はどうなりますか? 

実稼働環境の自動更新、追加のすべてのサンドボックス環境はキャンセルされます。 

### <a name="what-if-the-production-environment-is-manually-updated-after-the-production-environment-email-is-sent"></a>実稼働環境の電子メールが送られた後に、実稼働環境が手動で更新される場合はどうなりますか? 

実稼働環境の自動更新はキャンセルされますが、追加のすべてのサンドボックス環境はバージョン N に更新されます。

### <a name="what-if-i-find-an-issue-during-the-sandbox-update"></a>サンドボックスの更新中に問題が発生した場合はどうなりますか?

サンドボックス環境で検証を行うときに問題が見つかった場合は、有効なサポート チケット番号と業務の妥当性を提供することで LCS を通じて直接更新をスキップするように要求できます。 

### <a name="what-if-i-find-a-critical-issue-during-sandbox-testing-but-i-cant-pause-the-production-automatic-update"></a>サンドボックスのテスト中に重大な問題が見つかり、運用環境の自動更新プログラムを一時停止できない場合はどうなりますか?

識別されたらすぐに、重要な問題は常に LCS 経由でサポート チームに送信される必要があります。 サポート スタッフは、重要な問題に対する修正を行います。

### <a name="how-much-time-do-i-have-for-validation"></a>検証にかけることができる時間はどのぐらいですか?

更新がサンドボックス環境に適用されてから、7 暦日間検証できます。 もっと多くの時間が必要な場合、LCS のアクション センターを使用して配置可能なパッケージにアクセスし、環境に適用できます。 このようにして、生産ロールアウトよりも前に更新プログラムををテストするための追加の時間が得られます。

### <a name="what-happens-when-the-service-update-is-completed"></a>サービス更新プログラムが完了するとどうなりますか?

サービス更新プログラムが Microsoft によって適用された後、更新プログラムが成功したかどうか、または適用できなかったかどうかの通知を受け取ります。 更新プログラムを適用できないいくつかの理由があります。

- **保留中のパッケージ サインオフ**- パッケージがサインオフで保留中の場合、Microsoft はサービスの更新を実稼働環境に適用しません。
- **配置エラー** - 配置エラーが発生した場合、環境は元の状態にロールバックされます。
 
### <a name="if-there-is-a-failure-can-i-reschedule-the-update-to-be-automatically-applied"></a>失敗した場合、更新プログラムが自動的に適用されるように再スケジュールできますか?

実際には更新を再スケジュールすることはできません。 ただし、他の更新プログラムの適用をスケジュールするのと同じように、都合の良いときにパッケージを適用することができます。

### <a name="will-critical-hotfixes-be-automatically-applied-to-my-sandboxproduction-environment-during-automatic-update"></a>重要な修正プログラムは、自動更新中にサンドボックス/運用環境に自動的に適用されますか?

一般提供されてすべての顧客に自動適用されるサービス更新プログラムには、修正プログラムと潜在的な新しい機能が含まれます。 サービス更新プログラムが適用された後に重要な問題点が報告されると、顧客は LCS のタイルから累積的な修正プログラムを取り込むことができます。

### <a name="how-will-my-isvs-stay-current"></a>私の ISV は常に最新ですか?

顧客の環境のサービス更新プログラムには下位互換性があるため、独立系ソフトウェア ベンダー (ISV) によるアクションは必要ありません。 ISV は、そのコードが依存する最低限必要なプラットフォーム リリースを開発します。 重大な変更については、ISV が追加して検証するための 12 か月のリード タイムがあります。 ISV は、プラットフォーム ビットへの早期アクセスを獲得して、一般的に使用できるようになる前に更新プログラムに対するソリューションを検証できるようにするために、[パートナー早期アクセス プログラム](https://experience.dynamics.com/insider/)の一部とすることをお勧めします。

### <a name="what-about-new-features"></a>新機能はどうなりますか?

すべての新機能は、12 か月間オプトイン ベースで利用できます。 有効化を選択するまで変更管理は必要ありません。

### <a name="are-batch-jobs-suspended-during-a-service-update"></a>バッチ ジョブは、サービスの更新中に中断されますか?

バッチ ジョブはメンテナンス ウィンドウ中に中断され、メンテナンスの完了時に再開します。

更新プログラムを一時停止する方法の詳細については、[Lifecycle Services (LCS) によるサービスの更新の一時停止](../../dev-itpro/lifecycle-services/pause-service-updates.md)を参照してください。

## <a name="tools"></a>ツール

### <a name="how-can-i-get-early-access-to-non-released-platform-updates"></a>非リリースのプラットフォーム更新プログラムへの早期アクセスをどのように取得できますか。

はい、バージョン 10.0.26 から、すべてのサービス更新のプレビュー パッケージが、**ソフトウェア配置可能パッケージ** の下にある LCS の共有アセット ライブラリを通じてすべてのお客様が利用できるようになります。 プレビュー パッケージは、開発環境またはテスト環境に配置することができます。 これらは、運用環境では使用できません。 インストール時にプログラム規約に同意したものとします。 プレビュー パッケージ (旧プレビュー アーリー アクセス プログラム (PEAP)) へのアクセス登録は不要になりました。

[初回リリース プログラム](https://experience.dynamics.com/insider/)に参加できます。Microsoft は、常に最新の更新プログラムによってシステムを最新の状態に保ちます。 まだ Dynamics 365 Insider プログラムのメンバーとなっていない場合、次の作業が必要です。

1. この URL を使用してインサイダー プログラムにサインアップする: https://experience.dynamics.com
2. Dynamics 365 Insider になるための条件に同意します。
3. 申請が承認された後 (約 24 時間)、Insider Portal にサインインして、参加できるさまざまなプレビュー プログラムを検索することができます。

### <a name="is-any-tooling-available-to-support-testing-of-the-latest-release"></a>最新のリリースのテストをサポートするために使用可能なツールはありますか?

[Regression Suite Automation Tool](../../dev-itpro/lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md) は[現在利用可能](https://www.microsoft.com/download/details.aspx?id=57357)です。 このツールは、ユーザー受け入れテスト (UAT) の費用と時間を大幅に減少します。 通常、UAT は Microsoft アプリケーションの更新プログラムを取得するか、カスタム コードおよび構成を運用環境に適用する前に必要です。 機能パワー ユーザーはタスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくてもそれらを一連の自動テストに変換できます。 テスト ライブラリは、ビジネス プロセス モデラー (BPM) ライブラリを使用して LCS に保存および配分され、テストの実行、報告、調査のために Azure DevOps と完全に統合されます。 テスト データ パラメーターは、テスト ステップから切り離され、Excel データ ファイルに保存されます。

### <a name="how-can-i-test-and-validate-that-the-integrations-continue-to-work"></a>統合が機能し続けていることはどのようにテストおよび検証できますか?

データ タスクの自動化により、さまざまな種類のデータ タスクを簡単に繰り返し、各タスクの結果を検証することができます。 また、タスクの結果の検証を使用して、データ エンティティの自動テストを使用することもできます。 詳細については、[データ タスクの自動化](../../dev-itpro/data-entities/data-task-automation.md)の差し込みデータの概要を参照してください。

### <a name="how-can-i-determine-what-is-changed-in-a-service-update"></a>サービス更新プログラムの変更内容はどのようにわかりますか?

"新機能または変更点" のドキュメントは、各サービス更新プログラムサービスの詳細の主要ソースです。 [リリース計画](/business-applications-release-notes/)は、今後のリリースのすべての新機能と変更の情報の主要ソースです。 必要に応じて、機能には docs.microsoft.com のヘルプ トピックも含められます。 

### <a name="if-im-not-doing-active-developmentrecompilation-of-my-code-how-will-i-learn-whether-there-is-a-deprecated-feature-that-will-affect-me"></a>現在開発中でない、またはコードを再コンパイルしない場合、影響を受ける非推奨の機能があるかどうかはどうすればわかりますか? 

非推奨の機能については、リリースのたびに記載されます。 詳細については、[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) を参照してください。

## <a name="preparing-for-one-version"></a>1 つのバージョンの準備

### <a name="how-can-i-log-an-extensibility-request"></a>拡張機能の要求を記録するにはどうすればよいですか?

拡張機能の要求は、LCS に記録することができます。 詳細は、[機能拡張要求](../../dev-itpro/extensibility/extensibility-requests.md)トピックにあります。 使用可能な拡張機能の使用とログに関しては以下のタイムラインに注意してください。

| 日付         | 拡張機能の要求 |
|--------------|------------------------|
| 2019 年 1 月 | 拡張機能のすべての要求は、2019 年 1 月 1 日までにログインする必要があります。 ISV とユーザーは、この日までにコードを分析し、これらの要求を行ってください。 要求が 2019 年 1 月 1 日までに提出された場合、2019 年 4 月以降に 7.3 を維持するための例外が提供されます。 |
| 2019 年 12 月 | 2019 年 1 月 1 日までに記録された要求については、拡張機能は 2019 年 12 月 31 日以前に利用可能になります。 これらの拡張機能を使用しているユーザーは、2020 年 4 月までに現在のバージョンに移行する必要があります。 |

### <a name="what-does-end-of-service-mean"></a>サービスの終了にはどのような意味がありますか?

Microsoft は、サービスの終了に達したバージョンの問題を修正しません。 また、Microsoft は、3 つ以上のサービス更新プログラムより古いバージョンで発生した問題の調査とトラブルシューティングも行いません。 サービスの終了に達したバージョンで問題が発生した場合は、最新の更新プログラムに更新し、問題が解決されない場合はその問題を報告する必要があります。

すべての環境は、引き続き Microsoft によって運用されます。 監視や自動修復など、環境に関するすべての自動プロセスも、環境がサポートされているバージョンである限り、引き続きそのままです。

### <a name="will-individual-hotfixes-be-supported"></a>個別の修正プログラムをサポートしますか?

8.1 以降、個別の修正プログラムはサポートされません。 ユーザーは、最新の累積的な更新プログラムに更新して修正プログラム (8.1.1 など) を適用する必要があります。 さらに、重要な修正プログラムは累積的であり、LCS サービス エクスペリエンスを通じて使用可能になります。

### <a name="will-you-notify-me-about-critical-hotfixes-released-for-the-monthly-update-that-im-on"></a>利用している毎月の更新プログラムに関してリリースされる重要な修正プログラムに関する通知は送信されますか? 

顧客が報告した問題は、LCS 問題検索で検索できます。 未解決の問題が解決されたときに通知を受けるようにサインアップすることができます。

## <a name="commerce-service-updates"></a>コマース サービスの更新

### <a name="what-options-are-available-to-help-minimize-the-impact-on-my-commerce-cloud-components"></a>コマース クラウド コンポーネントへの影響を最小限に抑えるためにどのオプションを使用できますか?

コマース クラウド コンポーネントには、Dynamics 365 バックオフィスと同じダウンタイムが必要です。 今後のリリースでは、展開への更新を減らしてさらにスケジュールするために Retail Cloud Scale Unit (RCSU) が使用可能になります。 RCSU の詳細については、[ドキュメント](/business-applications-release-notes/October18/dynamics365-retail/planned-features)および、[リリース ノート](/business-applications-release-notes/?panel=products1#pivot=products)サイトにある発行済みのリリース情報を参照してください。

### <a name="will-there-be-options-to-take-individual-hotfixes-for-my-commerce-solution-components"></a>コマース ソリューション コンポーネントの個別の修正プログラムを取得するオプションはありますか?

コマース コンポーネントのすべての修正プログラムは累積的です。

### <a name="what-are-the-maintenance-downtime-requirements-that-might-affect-channel-operations"></a>チャンネル作業に影響を与える可能性のあるメンテナンス ダウンタイム要件は何ですか?

冗長性の業務ニーズがある小売業者のため、Modern POS オフライン機能では、インターネットから切断中またはクラウド環境の更新中にコア販売時点管理 (POS) 処理を使用できます。 Commerce Scale Unit を使用している店舗では、サポート クラウド メンテナンス期間中もコア POS 処理のサポートを伴う処理を継続します。 詳細については、[オンラインおよびオフライン販売時点管理 (POS) 処理](../../../commerce/pos-operations.md)を参照してください。

### <a name="when-will-i-have-to-update-my-in-store-components"></a>店舗内コンポーネントを更新する必要があるのはいつですか?

サポートを維持するために、店舗内のすべてのコンポーネントは、1 年以内にリリースされたソフトウェアを実行している必要があります。 ユーザーには、自己ホスト コンポーネントを更新し (店舗かプライベートで管理するデータ センターにインストールされているコンポーネントなど)、それらのコンポーネントのインストールされているバージョンが積極的にサポートされていることを確認する責任があります。

### <a name="will-there-continue-to-be-backward-compatibility-for-the-in-store-components"></a>店舗内コンポーネントの下位互換性は続行されますか?

クラウドにホストされているコンポーネントの更新では、そのバージョンのリリース日から 12 か月間、小売業者によって自己ホストされるコンポーネント バージョンとの下位互換性が保持され続けます。 (これらのコンポーネントには、Modern POS、Commerce Scale Unit、または Hardware Station などの店舗またはプライベート データセンターにインストールされるコンポーネントが含まれます。) ホスト型のコンポーネントは、クラウドホストのコンポーネントと同時に更新する必要はありません。 店舗外に更新を展開する時間をとるために、独立したリズムで更新を行うこともできます。

### <a name="what-options-are-available-for-updating-in-store-components-across-my-organization"></a>組織全体で店舗内コンポーネントを更新するためにどのようなオプションを使用できますか?

ユーザーは、店舗ごとに手動で自己ホストされているコンポーネントを更新するか、Microsoft System Center Configuration Manager や Microsoft Intune などの一括更新ツールを使用するかを選択できます。

### <a name="what-options-do-i-have-to-slowly-enable-new-functionality-across-my-channels"></a>チャネル全体で新しい機能を徐々に有効にするどのようなオプションがありますか?

Microsoft では、店舗、デバイス、およびユーザー全体で機能拡張を徐々に展開して有効にするいくつかのメカニズムを提供しています。

- **画面レイアウト デザイナー**: POS のほとんどのビジュアル要素は、顧客組織の管理ユーザーによって構成され、集中管理されます。 そのため、対応する画面レイアウトに含まれるように明示的に構成されていない限り、新しい POS の操作は POS に自動的に表示されません。 画面レイアウトは、画面レイアウト デザイナーを使用して構成され、店舗または POS デバイスに固有にすることができます。 詳細については、[販売時点管理 (POS) の画面レイアウト](../../../commerce/pos-screen-layouts.md)を参照してください。
- **機能プロファイル、POS のアクセス許可、コマース パラメーター** – POS の機能の重要な要素は通常、ユーザーがコンフィギュレーション可能です。 これらの要素は、機能プロファイル、POS のアクセス許可、Commerce パラメーター、または該当するシナリオにおけるデバイス レベル、レジスター レベル、店舗レベル、またはユーザー レベルの機能の管理を可能にするその他のコントロールを通じて構成できます。
- **Modern POS および Commerce Scale Unit** – Modern POS および Commerce Scale Unit は小売業者によって自己ホストされるため、いずれかのコンポーネントを含むトポロジによっては、個別 (および低速) のリズムかつクラウド専用トポロジより細かい方法での更新の展開が可能になります。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

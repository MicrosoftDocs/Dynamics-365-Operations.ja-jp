---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 28 (2019 年 7 月) の新機能および変更された機能
description: このトピックでは、 Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 28 (2019 年 7 月) でプレビューされる機能について説明します。
author: tonyafehr
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform 28
ms.openlocfilehash: 93994cf3939b4ee645f4cbbbbe891bcba3ef02fd
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863401"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-28-july-2019"></a>Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 28 (2019 年 7 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 28 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 7.0.5314 です。 プラットフォーム更新プログラム 28 の詳細については [追加リソース](whats-new-platform-update-28.md#additional-resources) を参照してください。

## <a name="data-management-enhanced-view-as-the-default-view"></a>データ管理拡張ビューを既定のビューにする
この数年間、データ管理において標準ビューの利用ができなくなっていました。 データ管理ワークスペースにアクセスするユーザーには、この期間中に機能が廃止になることが通知されていました。 拡張ビューが既定のビューとして設定されるようになりました。 標準ビューを引き続き使用することは可能であり、フレームワークパラメータの既存の設定を使用して元に戻すことも可能ですが、標準のビューは将来的に削除される予定であるため使用しないことを推奨します。 いずれかのデータ管理フォームで **標準ビュー** ボタンをクリックして標準ビューを使用すると選択した場合、個人用設定が適用されるため、引き続き標準ビューが表示されます。 しかし、拡張ビューの使用へ切り替えることを推奨します。

## <a name="preview-documents-using-embedded-pdf-viewer-control"></a>埋め込みPDF ビューア コントロール を使用してドキュメントをプレビューをする
Dynamics 365 for Finance and Operations においてドキュメントの表示処置を効率化するには、アプリケーション レポートの新しい 「プレビュー」 オプションを利用します。 埋め込みPDFドキュメントビューアーを使用することで、ローカル接続されているプリンターに直接アクセスし、画面の表示内容を忠実に紙に印刷します。 「Preview」 オプションは対応するすべての機器で使用可能であり、サードパーティ製のソフトウェアは必要ありません。 埋め込まれたPDFビューアーには、直感的な操作を提供する組み込みツールバーが用意されており、これによってドキュメントのダウンロードと閲覧が簡単になります。

## <a name="create-custom-commands-for-embedded-powerbicom-reports"></a>埋め込み PowerBI.com レポートにおける カスタムコマンドの作成
PowerBI.com レポートは、Dynamics 365 Finance and Operations のアプリケーションワークスペースで提供されています。カスタムメニューコマンドを使用することで、このレポートに表示されるグラフを視覚化し、洞察性を高めることができます。 直感的な操作によりレポート データのビューにフィルターをかけ、業務を行うことができます。 最新のプラットフォーム更新プログラムを適用すると、開発者は、Finance and Operations アプリケーション内で分析ソリューションと対話形式の実用的な操作体験をユーザーに提供するカスタム拡張機能を追加できます。

## <a name="extended-availability-of-the-legacy-navigation-bar"></a>従来のナビゲーションバーの拡張された可用性
プラットフォーム更新プログラム 24では、Dynamics 365 製品における Officeのヘッダーのビジュアルを統合する取り組みの一環として、刷新されたナビゲーションバーが Finance and Operations に導入されました。これには階層リンクは含まれていません。 この時点で、従来のナビゲーションバーは品質に影響をもたらす懸念から、優先除外スケジュール (Platform Update28以降は利用不可) に設定されていました。 新しいナビゲーションバーから パンくずリスト がなくなっていること関し、お客様からの不満が寄せられていることから、従来のナビゲーションバーの使用可能時期を2020年4月まで延長することを決定しました。 ナビゲーション バーの詳細、および従来 のナビゲーションバーに一時的に戻す方法については、 [更新されたナビゲーションバー](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar) を参照してください。 

## <a name="alert-users-before-sessions-end-due-to-inactivity"></a>非操作時間の経過によりセッションが終了する前にユーザーに警告する
Finance and Operations の既定のアイドルタイムアウトは、現在60分となっています。 ユーザーが非アクティブ状態の時間制限を超過した後は、セッションが終了したことをユーザーに警告します。 非アクティブによりセッションが中断されることをユーザーが認識し、保存されていない変更が失われないようにするために、非アクティブによるセッションのが了する3分前にユーザーに通知されるようになりました。 また、ユーザーはセッションが終了する前に再度セッションに接続することも可能です。  

## <a name="export-all-byod-job-name-changes"></a>すべての BYOD ジョブ の名称変更をエクスポートする
BYODの[すべての会社のエクスポート] ジョブの実行ジョブ構文に、命名規則にGUIDが追加されるようになりました。 これにより、名前が常に一意にになります。

## <a name="extensibility-enhancements"></a>拡張性の強化
プラットフォーム更新プログラム 28では、次の拡張機能が追加されました。

- それぞれの要素 (タスク、承認、自動化されたタスク)、およびイベントハンドラーを追加するには、WorkflowTypeの拡張機能を有効にします (Ref # 198838)。
- RelatedTableCardinality およびTableRelation TableRelation を変更するには、拡張機能を有効にします (Ref # 280969)。
- データ エンティティの国/地域コードの拡張機能を有効にします(Ref# 282123)。
- エンティティのフィールドのラベル、ヘルプテキスト、グループ プロンプト プロパティの拡張を有効にします (Ref # 265666) 。

## <a name="additional-resources"></a>追加リソース

### <a name="platform-update-28-bug-fixes"></a>プラットフォーム アップデート 28 のバグ修正プログラム
プラットフォーム更新 28 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=328737&dbType=3&qc=c3c678b3cdf18a7df3f284866ca4c5705b9e1e8df684b6db0222788c15fe1d2b)を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

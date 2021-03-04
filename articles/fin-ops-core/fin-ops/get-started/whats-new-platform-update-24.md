---
title: Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能および変更された機能
description: このトピックでは Dynamics 365 for Finance and Operation プラットフォーム更新プログラム 24 (2019 年 3 月) でプレビューできる機能について説明します。
author: tonyafehr
manager: AnnBe
ms.date: 03/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 20189-XX-XX
ms.dyn365.ops.version: Platform 24
ms.openlocfilehash: d50c3b8f3652f7adabf796c2a8c9b9663c7265ca
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797851"
---
# <a name="whats-new-or-changed-in-finance-and-operations-platform-update-24-march-2019"></a>Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 24 の新機能または変更された機能について説明します。 このバージョンのビルド番号は、7.0.5179 です。 プラットフォーム更新プログラム 24 の詳細については [追加リソース](whats-new-platform-update-24.md#additional-resources) を参照してください。

## <a name="new-apis"></a>新しい API

データ プロジェクトのインポート実行中に発生したエラーをデータ統合が取得するために、新しい API が追加されました。 これらの API は次のとおりです:

- GetImportTargetErrorKeysFileUrl
- GenerateImportTargetErrorKeysFile
- GetImportStagingErrorFileUrl 

詳細については、[データ管理パッケージ REST API](../../dev-itpro/data-entities/data-management-api.md)を参照してください。

## <a name="clear-identification-of-preview-builds"></a>プレビュー ビルドの明確な ID
一部のパートナー、ISV、および顧客は、Preview Early Access Program (PEAP) に参加することによって、またはサービスの公開プレビューを使用することによって、Finance and Operations の運用前ビルドにアクセスできます。 このプレビュー フェーズは、最新の機能についてのフィードバックおよびカスタマイズ検証のメカニズムとなることを意図しています。 ただし、これらの初期リリースは実稼働環境での使用を許可されていません。 Finance and Operations リリース プロセスの詳細については、[サービス更新の可用性](public-preview-releases.md) トピックを参照してください。

**プレビュー** ステータスをユーザーに明確にするために、各運用前ビルドは 2 つの異なる方法でタグ付けされます。 

- ナビゲーション バーには製品名の接尾語として「プレビュー」という単語が表示されます。  

    ![ナビゲーション バーのプレビュー インジケーター](media/previewCallout.png  "ナビゲーション バーのプレビュー インジケーター")  

- **情報** ボックスのタイトルには、「プレビュー」という単語が含まれます。 

    ![プレビューは情報ボックスにも表示されます](media/previewAboutBox.png  "プレビューは情報ボックスにも表示されます")
    

## <a name="updated-navigation-bar-that-aligns-with-the-office-header"></a>Office のヘッダーに対応した更新済みのナビゲーション バー
Dynamics 365 Office 製品は、各ヘッダーを Office ヘッダーと対応させて、Microsoft 製品全体のユーザーにとってよりまとまりのあるシェル エクスペリエンスを提供するよう取り組んでいます。 Finance and Operations のユーザーにとって、このヘッダー更新プログラムは、ナビゲーション検索をより目立つようにした、完全に再構成されたナビゲーション バーと見なされるでしょう。 特に、新しいデザインには階層リンクは含まれません。

更新されたナビゲーション バーは既定でプラットフォーム更新プログラム 24 に表示されます。 古いナビゲーションバーを使い続けたい顧客には、**クライアント パフォーマンス オプション** ページ、特に **レガシ ナビゲーション バー の有効化** 切り替えを使って一時的に行うことができます。 この切り替えはプラットフォーム更新プログラム 28 でのみ利用可能にする予定であり、その時点ですべてのお客様に最新のナビゲーション バーが表示されます。  

次の図は、プラットフォーム更新プログラム 24 の更新済のナビゲーション バーを表示します。

![プラットフォーム更新プログラム 24 の更新済のナビゲーション バー](media/updatedNavBar.png  "プラットフォーム更新プログラム 24 の更新済のナビゲーション バー")

次の図は、プラットフォーム更新プログラム 23 でナビゲーション バーがどのように表示されるかを示します。

![プラットフォーム更新プログラム 23 のナビゲーション バー](media/existingNavBar.png  "プラットフォーム更新プログラム 23 のナビゲーション バー")

## <a name="extensibility-enhancements"></a>拡張性の強化

プラットフォーム更新プログラム 24 に含まれる[プラットフォーム拡張機能の 1 番目の波](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility)は、2019 年 4 月リリース ノートにドキュメントされています。 9 つの拡張機能が詳細に説明されています。ハイライトの 1 つは、フォーム ボタン コントロールの新しい onClicking イベントです。

## <a name="client-alert-support-for-email-notifications"></a>電子メール通知のクライアント警告サポート
統合された変更追跡ツールで業務データを常に把握します。  プラットフォーム更新プログラム 24 を使用すると、あるイベントによってトリガーされたときに、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。  この機能は、Dynamic Ideas カスタマー フォーラムで最も求められている機能であると区別されています。  Dynamics 365 for Finance and Operations で、ユーザーはデータのフィルター処理されたビューを監視するためのカスタム警告ルールを定義できます。  電子メール通知を受信するオプションは、サポートされているすべての警告タイプで使用可能であり、既存の警告ルールでも有効にできます。  

サポートされるシナリオには、わかりやすいコントロールを使用して、システム バッチ ジョブのフィルター処理されたビューを監視する警告ルールを作成することが含まれます。  業務データへの変更についてのレポートを常にチェックするという負担から離れ、あなたに代わって Dynamics 365 for Finance and Operations インテリジェント変更検出サービスにモニタリングさせましょう。

## <a name="business-events-private-preview"></a>ビジネス イベント (プライベート プレビュー)
この新しい機能により、Finance and Operations の業務プロセスが実行されるときにビジネス イベントをキャプチャし、そのイベントを外部システムまたはアプリケーションに送信できるフレームワークが提供されます。

> [!Note]
> この機能はプライベート プレビューとして使用できます。 その機能が一般に利用可能になる時期については[リリース計画](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/planned-features)を参照してください。 

これにより、たとえば、発注書の承認によって、仕入先組織でのフルフィルメントがすぐにトリガーされるようになります。また破損部品の受領書 1 枚で、仕入先クレーム処理をリアルタイムでトリガーすることもできます。 これらのイベントは業務プロセスのコンテキストで発生するため、*ビジネス イベント* と呼ばれ、*業務プロセスの統合* が可能になります。

外部業務プロセスは、発生したときに通知を受けるために Finance and Operations の特定のビジネス イベントにサブスクライブします。 ビジネス イベントは Finance and Operations コネクタの「トリガー」としても使用できます。

含まれる予定の機能は次のとおりです。

-   ビジネス イベント フレームワーク、パートナーおよび顧客が実装するビジネス イベント。

-   ビジネス イベント管理者エクスペリエンス。

-   アプリケーション ビジネス イベント。

-   ワークフロー ビジネス イベント。

-   高度な統合シナリオのための Azure イベント グリッドおよび Azure Service Bus ですぐに使える統合。

-   Microsoft Power Automateでビジネス イベントを「トリガー」として公開する。

詳細については、[ビジネス イベントの概要](../../dev-itpro/business-events/home-page.md)を参照してください。

## <a name="additional-resources"></a>追加リソース
### <a name="platform-update-24-bug-fixes"></a>プラットフォーム アップデート 24 のバグ修正プログラム

プラットフォーム更新 24 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=287129&qc=6daf0a1b735f67d827cf6f643a2ef482dc0d66a220ce23ba6f3cba32ece56015)を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[Finance and Operations の削除または廃止された機能](../../dev-itpro/migration-upgrade/deprecated-features.md) トピックでは、Dynamics 365 for Finance and Operations の削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
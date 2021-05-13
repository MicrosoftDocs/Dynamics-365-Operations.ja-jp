---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 26 (2019 年 5 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 26 (2019 年 5 月) でプレビューされる機能について説明します。
author: tonyafehr
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-XX-XX
ms.dyn365.ops.version: Platform 26
ms.openlocfilehash: db657179d31337480c4fbf2f095dddd224ecd6b2
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923177"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-26-may-2019"></a>Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 26 (2019 年 5 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 26 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 7.0.5257 です。 プラットフォーム更新プログラム 26 の詳細については [追加リソース](whats-new-platform-update-26.md#additional-resources) を参照してください。

## <a name="business-events-generally-available"></a>一般的に利用可能なビジネス イベント
[ビジネス イベント](../../dev-itpro/business-events/home-page.md) は現在一般に利用できます。 これは、ビジネス イベントがプレビュー外であり、フライトを有効にすることなく既定で利用可能なことを意味します。 

## <a name="1n-support-for-microsoft-power-automate-to-subscribe-to-business-events"></a>Microsoft Power Automate の 1:N サポートでビジネス イベントを購読する
複数の Power Automate アプリが、同じ法人内の同じビジネス イベントを購読することができます。 [Microsoft Power Automate のビジネス イベント](../../dev-itpro/business-events/business-events-flow.md) は通知の送信や承認フローのトリガーなどのタスクに活用できます。 

## <a name="workflow-business-events"></a>ワークフロー ビジネス イベント
[ワークフロー ビジネス イベント](../../dev-itpro/business-events/business-events-workflow.md) は承認フローのトリガーに特に優れたターゲットです。 **ワークフロー作業項目** イベントは、 Power Automate の作業項目の完了を容易にする目的で、検証 および OData 完了アクションと組み合わせて使用できます。 作業項目の完成を促進する Power Automate テンプレートは進行中であり、関連するより多くの情報が近い将来 [ワークフロー ビジネス イベント](../../dev-itpro/business-events/business-events-workflow.md)ページで利用可能になります。

## <a name="business-events-are-idempotent"></a>ビジネス イベントは、べき等です
ビジネス イベントは、べき等です。 これはビジネス イベントのペイロードは、ControlNumber と呼ばれる一意で増え続ける番号を持つことを意味します。 この制御番号は、イベントの堅牢な処理を確実にするため、重複検出ロジックと故障出荷検出ロジックの適用に顧客が使用できます。

## <a name="azure-data-lake-integration---cdm-folder-and-model-improvements"></a>Azure Data Lake 統合 - CDM フォルダーとモデルの改善 
Azure Data Lake のエンティティ ストアは、プラットフォーム更新プログラム 25 のパブリック プレビューとして利用できます。 プラットフォーム更新プログラム 26 では、複数の環境で同じストレージ アカウントを使用できるようにフォルダ構造が改善されました。 また、エンティティ間の関係など追加のプロパティもモデルに含めました。 これは PowerBI.com によって導入された機能を使用して、モデルの関係を Power BI データセットに表示できます。

## <a name="feature-callouts"></a>機能のコールアウト
Finance and Operations の新しい機能が定期的に開発されています。 ドキュメントは新機能の説明に役立ちますが、役立つ場合にはユーザーの新機能に対する認識を製品内で直接高めます。 このために、プラットフォーム更新プログラム 26 で利用できる [機能のコールアウト](../../dev-itpro/user-interface/feature-callouts.md) はユーザーに新しい機能を示して、オプションで機能の詳細を知るためのハイパーリンクをユーザーに提供することができます。  

## <a name="extensibility-enhancements"></a>拡張性の強化
プラットフォーム更新プログラム 26 に含まれる [プラットフォーム拡張機能の 3 番目の波](/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility3) は、2019 年 4 月リリース ノートにドキュメントされています。 7 つの機能強化の詳細が説明されており、強調すべきひとつは、コマンド チェーンが他のメソッド拡張をターゲットにして拡張可能になったことです。

## <a name="additional-resources"></a>追加リソース

### <a name="platform-update-26-bug-fixes"></a>プラットフォーム アップデート 26 のバグ修正プログラム
プラットフォーム更新 26 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=313846&dbType=3&qc=a4ba239cdec6f528657f529750b68845b75580e5fdb0ad6060c4bc33f8da67f8)を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[Finance and Operations の削除または廃止された機能](../../dev-itpro/migration-upgrade/deprecated-features.md) トピックでは、Dynamics 365 for Finance and Operations の削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
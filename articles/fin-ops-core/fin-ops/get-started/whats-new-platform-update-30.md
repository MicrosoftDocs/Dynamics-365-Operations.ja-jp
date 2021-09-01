---
title: Finance and Operations アプリのプラットフォーム更新プログラム 30 (2019 年 11 月) の新機能および変更された機能
description: このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラム 30 の新機能または変更された機能について説明します。
author: tonyafehr
ms.date: 11/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: Platform update 30
ms.openlocfilehash: 3414e0cf5cbf9a8764402f96ddf4cc0aed56ba64f713063cb7d85491ac885a67
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734600"
---
# <a name="whats-new-or-changed-in-platform-update-30-for-finance-and-operations-apps-november-2019"></a>Finance and Operations アプリのプラットフォーム更新プログラム 30 (2019 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラム 30 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 7.0.5407 です。 一般提供開始日は 11 月ですが、新機能は 9 月の初期リリースで使用できます。 プラットフォーム更新プログラム 30 の詳細については [追加リソース](whats-new-platform-update-30.md#additional-resources) を参照してください。

## <a name="readable-date-time-format-for-datetime-fields-in-business-event-payload"></a>ビジネス イベント ペイロードの dateTime フィールドに対する読み取り可能な日時形式
新しいビジネス イベントがコード化されると、dateTime フィールドを有効にして、ビジネス イベント ペイロード人が判読可能な形式で値を出力することができます。 また、既存のビジネス イベントを変更して、ペイロードに読み取り可能な dateTime フィールドを含めることにより、互換性を維持することもできます。 開発者ドキュメントについては、[ビジネス イベント開発者ドキュメント](../../dev-itpro/business-events/business-events-dev-doc.md) で説明されています。

## <a name="hide-fields-much-faster-in-personalization-mode"></a>個人用設定モードでのより高速なフィールドの非表示
個人用設定モードでのフィールドの非表示が **大幅に** 速くなりました。 選択したコントロールを非表示にするシステムからの確認を待つ代わりに、このチェックが非同期に行われ、ユーザーがコントロールをクリックするのと同じ速さで非表示にできるようになりました。 この同じ最適化は、コントロールのスキップ、フィールドのロック、およびクイック タブ要約フィールドとしてのフィールドの追加にも適用されました。   

## <a name="extensibility-enhancements"></a>拡張性の強化
プラットフォーム更新プログラム 30 では、次の拡張機能が追加されました。

- 再拡張される拡張フィールド グループを含む、フォーム拡張シナリオの処理を改善します (Ref# 236593)。
- FormGridControl の既定のアクション プロパティを有効にして、拡張機能を通じて追加されたボタンを使用します (Ref# 322756)。
- フォーム データソースの削除イベントに対するポスト イベント ハンドラーをトランザクション スコープに追加します (Ref# 237952)。
- 警告を追加することにより、顧客やパートナーに "内部" クラスを拡張しないよう推奨します (Ref# 338010)。
- 複数のキー値および異なるタイプのキー値に対するより優れたサポートを追加して、X++ からの SysPlugin パターンの使用を改善します (Ref# 330178)。

## <a name="feature-class-property-added-into-metamodel-to-support-metadata-association-with-features-defined-for-feature-management"></a>機能管理用に定義された機能とのメタデータ関連付けをサポートするため、メタモデルに追加された機能クラス プロパティ
**機能クラス** プロパティはメタモデルに追加され、Visual Studio のアプリケーション エクスプローラーで複数のタイプで表示されます。 このプロパティは、機能管理に対して定義されている機能を示すルックアップです。 現在このプロパティは有効ではありませんが、開発者は将来このプロパティを使用して、対応する機能が機能管理ワークスペースで有効になった場合に、メタデータの一部だけがユーザーに表示されるようにします。 現在のところ、**機能クラス** プロパティが値に設定されている場合、ビルド警告が発生するため、開発者は効果がないことを認識しています。 新しいプロパティはメニューや MenuItems を含むいくつかのタイプで表示されますが、最終的にはフォーム、フォーム コントロール、およびその他のタイプでも表示されます。
将来、**機能クラス** プロパティ サポートを取得する最初のメタデータ タイプは、メニューとメニュー項目になります。それにより、対応する機能が有効になった場合に、開発者がそれらのメニュー オプションのみを使用できるようになります。 メニューとメニュー項目のランタイム サポートは、プラットフォーム更新プログラム 31 で提供されるようスケジュールされています。
現在のところ、機能クラス プロパティと FeatureStateProvider API を使用して、機能管理の既存の機能を参照できますが、追加機能を定義することはできません。 このサポートは、**機能クラス** プロパティ作業が完了した後に、有効になる可能性があります。 

## <a name="new-license-types-support-associating-users-with-a-license"></a>ユーザーとライセンスの関連付けをサポートする新しいライセンス タイプ
新しい顧客に対して新しいライセンス タイプが利用可能になります。 それらの新しいライセンスの顧客に関しては、ユーザーをライセンスに関連付ける必要があります。 ライセンスが新しいユーザーに関連付けられている場合、初めてサインインしたときにシステム ユーザーとして追加されます。 ライセンスがユーザーに関連付けられていない場合は、簡単な警告が表示されます。


## <a name="additional-resources"></a>追加リソース

### <a name="platform-update-30-bug-fixes"></a>プラットフォーム アップデート 30 のバグ修正プログラム
プラットフォーム更新 30 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?kb=4520346&bugId=369591&dbType=3&qc=a1f7377056b8d98314a62c745da88565f03531d15de24c4a538132d68118059c)を参照してください。

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2019wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[Finance and Operations の削除または廃止された機能](../../dev-itpro/migration-upgrade/deprecated-features.md)トピックでは、削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Finance and Operations バージョン 10.0.1 (2019 年 4 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations バージョン 10.0.1 の新機能または変更された機能について説明します。 このバージョンは 4 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: a362a31d-44df-45c5-b698-64c5264c592e
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: b57c2434fdb19f707125ec24cac76a72bd90bfee
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "975739"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-1001-april-2019"></a>Finance and Operations バージョン 10.0.1 (2019 年 4 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 の新機能または変更された機能について説明します。 このバージョンは 4 月にリリースされ、ビルド番号は 10.0.51 です。 バージョン 10.0.1 の詳細については [追加リソース](whats-new-changed-10-0-1.md#additional-resources) を参照してください。

最新のリリースの Microsoft Dynamics 365 for Retail の新機能と変更については、[Dynamics 365 for Retail バージョン 10.0.1 の新機能と変更](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/whats-new-10-0-1) を参照してください。


## <a name="enable-edit-for-externally-maintained-fields"></a>外部管理フィールドの編集を有効化

見込顧客リストの現金化への統合など、外部システムとの統合シナリオのため、グローバル アドレス帳および顧客レコードの特定のフィールドは、外部システムで管理されることを予想して外部管理とマークされています。 **外部管理フィールドの編集を有効化** オプションがグローバル アドレス帳パラメータ (**組織管理 > グローバル アドレス帳 > グローバル アドレス帳パラメータ**) に既定値の **いいえ** で追加されました。  ユーザー シナリオでこれらのフィールドを外部管理の場合も編集可能にする必要がある場合は、値を **はい** に設定できます。

## <a name="regulatory-updates"></a>規制の更新
Finance and Operations の規制の更新については、[ローカライズおよび規制機能 – 規制の更新](../../financials/localizations/regulatory-updates.md) を参照してください。 また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。


## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
Finance and Operations 10.0.1 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=299640&dbType=3&qc=2da6de70aab0f4c61b0f920b3242211f5043697189d50a6e1fb1ac3d27ee5f78)を参照してください。

### <a name="platform-update-25"></a>プラットフォーム update 25
Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 には、プラットフォーム更新プログラム 25 が含まれています。 プラットフォーム更新プロフラム 25 の詳細ついては [Finance and Operations プラットフォーム更新プログラム 25 (2019 年 4 月) の新機能や変更](whats-new-platform-25.md) を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


---
title: Finance and Operations バージョン 10.0 (2019 年 4 月) の新機能および変更された機能
description: このトピックでは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 のプレビュー中の機能について説明します。 このバージョンは、2019 年 4 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: Release 10
ms.openlocfilehash: 3e7c99b374cf74325ecee9993038a2035add23d2
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "777119"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-100-april-2019"></a>Finance and Operations バージョン 10.0 (2019 年 4 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 10.0.8 です。 バージョン 10.0 の詳細については [追加リソース](whats-new-changed-10.md#additional-resources) を参照してください。

Microsoft Dynamics 365 for Retail の機能については [Dynamics 365 for Retail (2019 年 4 月) の新機能および変更された機能](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/april-whats-new) を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化

Finance and Operations の今回のリリースでは、列挙、メタデータ、メソッドの強化など、拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。 詳細については、[Dynamics 365 for Finance and Operations バージョン 10.0 で変更された拡張機能](../../dev-itpro/extensibility/extensibility-changes-10.md)を参照してください。

## <a name="catch-weight-product-processing-with-warehouse-management"></a>倉庫管理による CW 製品の処理
この機能を使用すると、倉庫管理プロセス内の CW 製品を使用できます。 この機能は、今回のリリースの制限対象者のみに提供できます。 

詳細については、[倉庫管理の CW 製品処理](../../supply-chain/warehousing/catch-weight-processing.md) を参照してください。

## <a name="non-gst-transactions-for-india"></a>インド向けの非販売税トランザクション 
この機能を使用すると、税エンジンを使用して非販売税トランザクションを作成できます。 非販売税トランザクションを作成するには、それぞれの課税対象トランザクション行の **税情報** で **非販売税** チェック ボックスを選択します。 また、**参照番号順序グループ** に **供給の請求** の **番号順序コード** があることも確認する必要があります。 これらのトランザクションは、販売税還付 (GSTR) で非販売税トランザクションとして識別されます。 

## <a name="regulatory-updates"></a>規制の更新
Finance and Operations の規制の更新については、[ローカライズおよび規制機能 – 規制の更新](../../financials/localizations/regulatory-updates.md) を参照してください。 また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
Finance and Operations 10.0 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2080156)を参照してください。

### <a name="platform-update-24"></a>プラットフォーム update 24
Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 には、プラットフォーム更新プログラム 24 が含まれています。 プラットフォーム更新プロフラム 24 については [Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能と変更された機能](whats-new-platform-update-24.md) を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

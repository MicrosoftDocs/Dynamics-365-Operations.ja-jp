---
title: Dynamics 365 Finance バージョン 10.0.8 (2020 年 1 月) のプレビュー機能
description: このトピックでは、Dynamics 365 Finance バージョン 10.0.8 の新機能または変更された機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 20a1a337c92d8f270ee95d0c076ce07fe5696a47
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945871"
---
# <a name="preview-features-in-dynamics-365-finance-version-1008-january-2020"></a>Dynamics 365 Finance バージョン 10.0.8 (2020 年 1 月) のプレビュー機能

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.8 用 Finance and Operations 向けプラットフォーム更新プログラム 32 の新機能または変更されたプレビュー機能について説明します。 このバージョンのビルド番号は 8.0.xxxx で、次のように使用できます。

- 2019 年 11 月プレビュー リリース。
- 2020 年 1 月の一般提供 (自己更新)。
- 2020 年 2 月の自動更新が進行中です。

プラットフォーム更新プログラム 32 の詳細については [追加リソース](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md#additional-resources) を参照してください。

## <a name="feature-name"></a>機能名

説明 

## <a name="expense-receipt-processing"></a>経費の領収書

[!NOTE]
> - この機能では現在、英語の領収書のみがサポートされています。
> - この機能は現在、米国のみでサポートされています。
> - この機能では、ユーザー データを学習の構築に使用することはありません。 アップロードした領収書に基づかない、領収書処理用の一般的な機械学習モデルを構築してきました。
> - Dynamics 365 Finance では、フィールド データを抽出するために Cognitive Services に手を差し伸べ、Cognitive Services は処理が完了するまで最大 24 時間、領収書のコピーが保持されます。 完了した Cognitive Services で、領収書が削除されます。 領収書は、Dynamics 365 Finance に格納されます。 参照 [Form Recognizer の新機能を使用して領収書を理解する](https://azure.microsoft.com/en-us/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)

経費レポートの作成時にエンド ユーザー エクスペリエンスを向上させるために設計された、 領収書 OCR 処理の導入により経費入力が強化されました。

主要な機能:
- 領収書からマーチャント名、日付、合計金額を抽出する
- 領収書を経費トランザクションに一致させるように試行する

この機能は、**経費レポート再想像**機能を使用してサポートされています。 この機能を有効にするには、**機能管理** ワークスペースを使用して、**経費レポートを再想像**し、**自動照合を有効にして、領収書機能から経費を作成します**。

詳細については、[経費精算書の再設計](ExpenseWorkspaceNew.md) を参照してください。



## <a name="additional-resources"></a>追加リソース

### <a name="platform-update-xx"></a>プラットフォーム更新プログラム xx

Microsoft Dynamics 365 Supply Chain Management 10.0.8 には、プラットフォーム更新プログラム 32 が含まれています。 プラットフォーム更新プログラム xx の詳細については、[プラットフォーム更新プログラム 32 のプレビュー機能](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-xx.md)を参照してください。


### <a name="bug-fixes"></a>バグ修正 
10.0.7 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=386529&dbType=3&qc=e03ced97fa18dc4439f36de17b00da7257dc15869a72e5b2435fec0acec0c493) を参照してください。


### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

---
title: Dynamics 365 Commerce 10.0.28 (2022 年 7 月) の新機能または変更された機能
description: この記事では、Dynamics 365 Commerce 10.0.28 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 05/26/2022
ms.topic: article
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: afd702244a86fbe5572c403e8819f17f8a20c642
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869445"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10028-july-2022"></a>Dynamics 365 Commerce 10.0.28 (2022 年 7 月) の新機能または変更された機能

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 10.0.28 の新機能または変更された機能を示します。 このバージョンのビルド番号は 10.0.1227 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 5 月
- **リリースの一般提供 (手動更新):** 2022 年 7 月
- **リリースの一般提供 (自動更新):** 2022 年 7 月


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域                             | フィーチャー                                         | 詳細                                                           |   に  によって有効化             |
|-------------------------------------------|----------------------------------------------------------|-----------------------------------------------------------|-------------------------|
|  Commerce SDK   |   価格設定および割引のカスタマイズ  |  Commerce SDK での価格設定と割引のカスタマイズをサポートするために、**Microsoft.Dynamics.Commerce.Runtime.Services.PricingEngine.Contracts** パッケージが、価格決定契約および割引契約を消費する拡張コードのパブリック フィードに公開されます。  |  [Commerce SDK への移行](../dev-itpro/retail-sdk/migrate-commerce-sdk.md#reference-package-difference-between-legacy-retail-sdk-and-commerce-sdk) を参照
|  展開 | Dynamics 365 Commerce Cloud Scale Unit (CSU) 拡張機能および eコマース パッケージの展開   |  バージョン 3.* 以降では、Dynamics Lifecycle Services (LCS) **アセット配置** タスクはコマース パッケージの展開をサポートします。 **資産のタイプ** という名前の新しいフィールド タイプが追加されたため、コマース パッケージの配置タイプを選択できます。 以下の値は、このフィールドで使用できます:</p><p>- **ソフトウェア配置可能パッケージ**: 財務と運用アプリの環境配置 (既定値)<p>- **Commerce Cloud Scale Unit 拡張機能**: CSU 拡張機能パッケージの展開<p>- **eコマース パッケージ**: eコマース環境の配置<p>**Commerce Cloud Scale Unit 拡張機能 - CSU 拡張機能パッケージの配置** または **eコマース パッケージ - eコマース環境の配置** オプションのいずれかを選択すると、以前の展開より優先されます。 複数の CSU 拡張機能パッケージがある場合は、すべての CSU パッケージを配置用の 1 つのパッケージとしてマージする必要があります。  | [Azure Pipelines を使用した資産のデプロイ](../../fin-ops-core/dev-itpro/dev-tools/pipeline-deploy-asset.md) を参照  |
| 支払   |  Adyen 向け Dynamics 365 Payment Connector を使用した Google Pay   |  e コマースの顧客は、エクスプレス チェックアウト モジュールで構成されたカートとチェックアウトのページで Google Pay を使用できます。   |  開発者のオプトイン   |

## <a name="additional-resources"></a>追加リソース

Dynamics 365 Finance 10.0.28 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.28 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

この更新プログラムに含まれるバグの修正については、Lifecycle Services (LCS) にサインインし、[サポート技術情報の記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

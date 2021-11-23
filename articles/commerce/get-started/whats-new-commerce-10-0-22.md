---
title: Dynamics 365 Commerce 10.0.22 (2021 年 11 月) の新機能と変更された機能
description: このトピックでは、Dynamics 365 Commerce 10.0.22 のプレビュー リリースの新機能または変更された機能について説明します。
author: josaw1
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-09-31
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 9bec57e88c82965a1ad38bb6c29501dd51fcf333
ms.sourcegitcommit: 76fe020f9c5f4e5cc2e93f5ccb3b040f12b0363e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2021
ms.locfileid: "7749523"
---
# <a name="whats-new-and-changed-in-dynamics-365-commerce-10022-november-2021"></a>Dynamics 365 Commerce 10.0.22 (2021 年 11 月) の新機能と変更された機能

[!include [banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 Commerce 10.0.22 の新機能または変更された機能について列挙します。 このバージョンのビルド番号は 10.0.995 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 9 月
- **リリースの一般提供 (手動更新):** 2021 年 10 月
- **リリースの一般提供 (自動更新):** 2021 年 11 月


## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。 各機能の公式リリース日については、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/finance-operations-crossapp-capabilities/planned-features) を参照してください。 このトピックが最初に公開された後に、ビルドに加えた機能を含めるために、このトピックを更新することがあります。 機能を有効にする方法を確認するには、次のテーブルで **有効化** 列を参照してください。 機能管理の使用方法の詳細については、[機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を参照してください。

| 機能領域   | フィーチャー                                                  | 詳細                                          |   に  によって有効化             |
|----------------|----------------------------------------------------------|-----------------------------------------------------------|-------------------------|
|  顧客管理 | 在庫を意識した製品検索用のサイト ビルダー コンフィギュレーション | [店舗内の顧客管理](../customer-mgmt-stores.md) | 機能管理 |
|  顧客注文  |  [ゲスト清算の注文検索を有効にする](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/enable-order-lookup-guest-checkouts)    |  [ゲスト清算の注文検索を有効にする](../order-lookup-guest.md)<p>[注文検索モジュール](../order-lookup-module.md)</p> |  機能管理   |
|  E コマース      |   [eコマース サイト用の地域検出およびリダイレクト](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/geo-detection-redirection-e-commerce-sites) | [地域の検出とリダイレクトを設定する](../geo-detection-redirection.md)<p>[国/地域の選択モジュール](../country-region-picker-module.md)</p>   |                    サイト ビルダーの設定    |
| 拡張性 | Lifecycle Service なしで Dynamics 365 Commerce の独自のローカル開発環境を設定する | [独自のローカル開発環境を設定する](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit/tree/release/9.32/src/ScaleUnitSample/.vscode) | |
| 拡張性 | Visual Studio Code を使用して Commerce Cloud Scale Unit (CRT および API) 拡張機能を開発する | [VS Code を使用して CSU 拡張機能を開発する](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit/tree/release/9.32/src/ScaleUnitSample/.vscode) | |
| グローバリゼーション | (イタリア) 抽選コードの検証 | 顧客マスター レコードまたは販売トランザクションに対して指定された抽選コードの検証は、対応する登録タイプに対して定義されている形式に基づいて行われます。 詳細については、[抽選コードの登録タイプの設定](../localizations/emea-ita-customer-information.md#set-up-a-registration-type-for-the-lottery-code)を参照してください。 | 既定で有効 |
| 販売促進 | 最適化された製品可用性の計算 | [小売チャンネルの引当可能在庫数量の計算](../calculated-inventory-retail-channels.md) | 機能管理 |
| 販売促進 | [評価とレビューに対してモデレーターを必須にする](/dynamics365-release-plan/2021wave2/commerce/dynamics365-commerce/require-moderator-ratings-reviews) | [モデレーターによる評価とレビューの手動公開を有効化する](../manual-publish-rating-reviews.md) | サイト ビルダーの設定  |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.22 には、プラットフォーム更新プログラムが含まれています。 詳細については、[Finance and Operations アプリのバージョン 10.0.22 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299) を参照してください。

Commerce 固有の重大な変更を加える場合は、[Dynamics 365 Commerce オンライン SDK に関するよく寄せられる質問](../e-commerce-extensibility/sdk-faq.md) を参照してください。

### <a name="dynamics-365-2021-release-wave-2-plan"></a>Dynamics 365: 2021 リリースのウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)トピックでは、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Dynamics 365 Commerce 10.0.18 (2021 年 5 月) の新機能と変更された機能
description: この記事では、Dynamics 365 Commerce 10.0.18 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 661ff0cd12ac2bea88f5506489825faf42b74720
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862236"
---
# <a name="whats-new-and-changed-in-dynamics-365-commerce-10018-may-2021"></a>Dynamics 365 Commerce 10.0.18 (2021 年 5 月) の新機能と変更された機能

[!include [banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 Commerce 10.0.18 の新機能または変更された機能を示します。 このバージョンのビルド番号は 10.0.793 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2021 年 3 月
- **リリースの一般提供 (自己更新):** 2021 年 4 月
- **リリースの一般提供 (自動更新):** 2021 年 5 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。 機能タイトルは、[リリース計画](/dynamics365/release-plans/)のサイトに関する追加情報にリンクします。 追加のリンクは、その機能に対して現在使用可能な追加のドキュメントを指します。 これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

- AJAX を含むサーバー側データ アクションの呼び出し<br> - 詳細については、[AJAX を使用したサーバー側のデータ アクションの呼び出し](../e-commerce-extensibility/data-actions-with-ajax.md) を参照してください
- トランザクションとレシートの電子メールへの QR コードまたはバー コードの追加<br> - 詳細については、[トランザクションとレシートの電子メールへの QR コードまたはバー コードの追加](../add-qr-code-barcode-email.md) を参照してください
- [カスタム レイアウトおよびテンプレートを使用するためのレシートの電子メールのコンフィギュレーション](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/email-receipt-improvements-new-features)<br> - 詳細については、[カスタム レイアウトおよびテンプレートを使用するためのレシートの電子メールのコンフィギュレーション](../configure-emailed-receipt-formats.md) を参照してください
- Commerce オンライン SDK に関するよく寄せられる質問への追加<br> - 詳細については、[Dynamics 365 Commerce オンライン SDK に関するよく寄せられる質問](../e-commerce-extensibility/sdk-faq.md) を参照してください
- [GitHub と NuGet から Retail SDK サンプルと参照パッケージをダウンロードする](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/simplified-commerce-sdk-update-developer-experience)<br> - 詳細については、[GitHub と NuGet から Retail SDK サンプルと参照パッケージをダウンロードする](../dev-itpro/retail-sdk/sdk-github.md) を参照してください
- [E コマースの在庫 API から販売の測定単位 (UoM) で数量を取得する](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/enhancements-e-commerce-inventory-availability-lookup-apis)<br> - 詳細については、[小売チャンネルの引当可能在庫数量の計算](../calculated-inventory-retail-channels.md) を参照してください
- [POS 在庫検索操作に関する強化事項](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/improvements-pos-inventory-lookup-operation)
- [新しいクラウド検索インフラストラクチャを使用した、高パフォーマンスでスケーラブルな顧客検索エクスペリエンス](/dynamics365-release-plan/2021wave1/commerce/dynamics365-commerce/highly-performant-scalable-customer-search-experience-using-new-cloud-search-infrastructure)

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Dynamics 365 Commerce 10.0.18 には、プラットフォーム更新プログラムが含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.18 のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正 
この更新プログラムに含まれるバグ修正については、Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=561679&dbType=3&qc=13bb1641c1be430ead8b21ae3d4e0f800d5b81c39b3a56e890db1de7ede59e46) を参照してください。

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2021wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
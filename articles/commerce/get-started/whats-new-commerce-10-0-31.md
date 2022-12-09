---
title: Dynamics 365 Commerce 10.0.31 (2023 年 2 月) のプレビュー
description: この記事では、Microsoft Dynamics 365 Commerce 10.0.31 の新機能および変更された機能について説明します。
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: ed4325095163415d05a56128cb1f0334440fe0e5
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787529"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Dynamics 365 Commerce 10.0.31 (2023 年 2 月) のプレビュー

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce プレビュー バージョン 10.0.31 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1406 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 10 月
- **リリースの一般提供 (手動更新):** 2023 年 1 月
- **リリースの一般提供 (自動更新):** 2023 年 2 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに追加された機能を含めるために、この記事を更新することがあります。

| 機能領域 | 機能 | 詳細 |  に  によって有効化 |
|---|---|---|---|
| エラー コード | Commerce では、オンライン買い物客に表示されるオンライン チャンネルのチェック アウト エラーに含まれる標準化されたエラー参照が導入されています。| [チェックアウト モジュールのエラー コード](../checkout-module-error-codes.md)  | 既定で有効 |
| 支払 | [Adyen 向け Dynamics 365 Payment Connector で Apple Pay を有効にする](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | eコマース顧客は、サポートされているデバイスまたはブラウザを使用する際に、カートやチェックアウト ページで Apple Pay を使用できます。 | 開発者のオプトイン |
| 支払  |  Commerce では、Commerce Headquarters ユーザー インターフェイス全体でユーザーが定期的な支払トークンをどう処理するのかを制限する機能が追加されました。 **コール センター販売注文** ページなどの支払フォームには、顧客が以前に使用した定期的な支払いのトークンが新しいトランザクション用に表示されなくなりました。 Commerce の **顧客支払** 画面で決定された "ファイルのカード" 入力のみ、または販売注文を通して支払い中に顧客が合意した場合のみ、新しいトランザクションの支払処理時にコール センターまたは Commerce Headquarters のユーザーに提示されます。 | [支払トークンの使用の制限](../dev-itpro/limit-token-usage.md)  |  機能管理<p>*支払トークンの使用を注文コンテキストに制限する*  |
| POS | [POS から発注書を作成する](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  ユーザーが発注書要求を作成、編集、および確認できるよう、販売時点管理 (POS) でインバウンド在庫操作を改善しました。 |  機能管理<p>*POS で発注書要求を作成する機能*   |
| その他の言語が利用可能になりました | 4 つの言語が追加されました | 優先言語リストでユーザーが選択できる言語が 4 つ追加されました: 韓国語、ポルトガル語 (ポルトガル)、ベトナム語、および中国語 (繁体字)。 このオプションを選択するには、**ユーザー オプション \> 基本設定 \> 国/地域の設定** に移動します。 | ローカライズされた基本設定 |  



## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Commerce 10.0.31 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.31 のプラットフォーム更新プログラム (2023 年 2 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md) を参照してください。 
  

### <a name="bug-fixes"></a>バグ修正

バージョン 10.0.31 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Microsoft Dynamics Lifecycle Services (LCS) にサインインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 および業界のクラウド: 2022 年リリース ウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 2 プラン](/dynamics365-release-plan/2022wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-commerce-features"></a>削除され、非推奨の Commerce 機能

[Dynamics 365 Commerce で削除または廃止された機能](removed-deprecated-features-commerce.md)の記事では、Commerce で削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Commerce の削除済みまたは非推奨の機能](removed-deprecated-features-commerce.md)の記事に発表されます。


コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

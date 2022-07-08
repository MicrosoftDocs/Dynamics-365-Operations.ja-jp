---
title: Dynamics 365 Commerce サンドボックス環境の構成
description: この記事では、Microsoft Dynamics 365 Commerce のサンドボックス環境をプロビジョニング後に構成する方法について説明します。
author: psimolin
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 259a580981003f135e234f66e9e93ceb18605412
ms.sourcegitcommit: 252cb41c3029b623354698463f7b44a29fd9f184
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013112"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>Dynamics 365 Commerce サンドボックス環境の構成

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce のサンドボックス環境をプロビジョニング後に構成する方法について説明します。

この記事に記載の手順は、コマースのサンドボックス環境がプロビジョニングされた後でのみ着手してください。 Commerce サンドボックス環境をプロビジョニングする方法については、[Commerce サンドボックス環境のプロビジョニング](provisioning-guide.md) を参照してください。

Commerce サンドボックス環境をエンドツーエンドでプロビジョニングした後、環境の使用する前に、追加のプロビジョニング後の構成手順を完了する必要があります。 これらの手順を完了するには、Microsoft Dynamics Lifecycle Services (LCS) と Dynamics 365 Commerce を使用する必要があります。

## <a name="before-you-start"></a>始める前に

1. [LCS ポータル](https://lcs.dynamics.com) にサインインします。
1. プロジェクトに移動します。
1. リストで環境を選択します。
1. 右側の環境情報で、**環境にログインする** を選択します。 コマースの本部に送信されます。
1. 右上隅にある **USRT** 法人が選択されていることを確認します。 この法人は、デモ データに事前構成されています。
1. **Commerce パラメーター \> 構成パラメーター** に移動、**ProductSearch.UseAzureSearch** のエントリがあり、値が **true** に設定されていることを確認します。 この項目がない場合は、追加して値を **true** に設定してください
1. **小売とコマース \> 小売とコマース \> コマース スケジューラ \> コマース スケジューラの初期化** の順に移動します。 **コマース スケジューラの初期化** ポップアップ メニューで、**既存のコンフィギュレーションの削除** オプションを **はい** に設定し、**OK** を選択します。
1. ストアと eコマースチャネルを正しく動作させるには、Commerce Scale Unit に追加する必要があります。 **小売とコマース \> 本社の設定 \>  コマース スケジューラ  \> チャネル データベース** の順に移動し、左のペインで、Commerce Scale Unit を選択します。 これらの eコマース チャネルを使用する場合は、**小売チャネル** FastTab で、**AW オンライン ストア**、**AW Business オンライン ストア**、および **Fabrikam 拡張オンライン ストア** のチャンネルを追加します。 必要に応じて、販売時点管理 (POS) を使用する場合 (たとえば、**シアトル**、**サンフランシスコ**、**サンホセ**) は、小売店舗を追加することもできます。
1. すべての変更をチャンネル データベースと同期するには、Commerce Scale Unit で **チャンネル データベース \>の完全データ同期**  を選択します。

コマース本部でのプロビジョニング後の活動では、法人として **USRT** が常に選択されていることを確認してください。

## <a name="configure-the-point-of-sale"></a>販売時点管理を構成する

### <a name="associate-a-worker-with-your-identity"></a>作業者と ID の関連付け

作業者を ID に関連付けるには、コマース本部で次の手順を実行します。

1. 左側のメニューを使用して、**モジュール \> 小売とコマース \> 従業員 \> 作業者** の順に移動します。
1. リストで、次のレコードを検索し、選択します: **000713 - アンドリュー コレット**。 この例のユーザーは、次のセクションで使用するサンフランシスコの店舗に関連付けらたユーザーです。
1. アクション ウィンドウで、**コマース** を選択します。
1. **既存の ID の関連付け** を選択します。
1. **電子メールを使用した検索** の右にある **電子メール** フィールドに、電子メール アドレスを入力します。
1. **検索** を選択します。
1. 名前を含むレコードを選択します。
1. **OK** を選択します。
1. **保存** を選択します。

### <a name="activate-cloud-pos"></a>クラウド POS の有効化

LCS のクラウド POS を有効にするには、LCS で次の手順を実行します。

1. トップ メニューで、**クラウド ホスト環境** を選択します。
1. リストで環境を選択します。
1. 右側の環境情報で、**クラウド販売時点管理にログインする** を選択します。
1. **次へ** を選択し て、**開始する前に** ダイアログ ボックスを開きます。
1. **サーバー URL** フィールドに変更は必要ありません。 **次へ** を選択します。
1. Microsoft Azure Active Directory (Azure AD) アカウントを使用してサインインします。
1. **店舗名** 配下で、 **サンフランシスコ** を選択し、**次へ** を選択し ます。
1. **レジスターとデバイス** で、**SANFRAN-1** を選択します。
1. **有効化** を選択します。 サインアウトして、POS のサインイン ページに移動します。
1. オペレーター ID **000713** およびパスワード **123** を使用して、クラウド POS エクスペリエンスにサインインできるようになりました。

## <a name="set-up-your-e-commerce-sites"></a>eコマース サイトを設定します

Fabrikam、Adventure Works、Adventure Works Business の 3 つの eコマースのデモ サイトがあります。 次の手順に従って、各デモ サイトを構成します。

1. プロビジョニングの実行時に eコマースを初期化した際に作成した URL を使用して、コマース サイトの管理ツールにサイン インします ([eコマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。
1. サイト (**Fabrikam**、**Adventure Works**、**Adventure Works Business**) を選択して、サイトの設定ダイアログ ボックスを開きます。
1. コマースを初期化したときに入力したドメインを選択します。
1. 本社で、既定のチャンネルに対応する構成済みのオンライン店舗チャンネル (**Fabrikam 拡張オンライン店舗**、**AW オンライン店舗**、**AW Business オンラインストア**) を選択します。
1. 既定の言語として **en-us** を選択します。
1. パス フィールドを構成します。 1 つのサイトに対して空白のままにすることができますが、複数のサイトに同じドメイン名を使用する場合は、構成する必要があります。 たとえば、ドメイン名が `https://www.constoso.com` の場合、Fabrikam (`https://contoso.com`) には空白のパスを使用し、Adventure Works (`https://contoso.com/aw`) には「aw」、Adventure Works (`https://contoso.com/awbusiness`) のビジネス サイトには「awbusiness」を使用することができます .
1.  **OK** を選択します。 サイトでページのリストが表示されます。
1. 必要に応じて、手順 2-7 を繰り返して他のデモ サイトを構成します。

## <a name="enable-jobs"></a>ジョブの有効化

コマースのジョブを有効化するには、次の手順に従います。

1. 本部環境にサインインします。
1. 左側のメニューを使用して、**小売とコマース \> 照会およびレポート \> バッチ ジョブ** の順に移動します。

    この手順の残りの部分は、次の各ジョブに対して完了する必要があります。

    * 小売用の注文電子メール通知の処理
    * 製品の使用可能性
    * P-0001
    * 注文ジョブを同期します

1. クイック フィルターを使用して、名前でジョブを検索します。
1. ジョブの状態が **実行中** の場合、次の手順を実行します。

    1. レコードを選択します。
    1. アクション ウィンドウの、**バッチ ジョブ** タブで、**状態の変更** を選択します。
    1. **キャンセル** を選択し、**OK** を選択します。

1. ジョブの状態が **源泉徴収** の場合、次の手順を実行します。

    1. レコードを選択します。
    1. アクション ウィンドウの、**バッチ ジョブ** タブで、**状態の変更** を選択します。
    1. **待機中** を選択し、**OK** を選択します。

必要に応じて、以下のジョブの繰り返し間隔を1分に設定することも可能です。

* 小売用の注文電子メール通知ジョブの処理
* P-0001 ジョブ
* 注文ジョブを同期します

### <a name="run-full-data-synchronization"></a>完全データ同期の実行

コマースで完全なデータ同期を実行するには、コマース本部で次の手順を実行します。

1. 左側のメニューを使用して、**モジュール \> 小売とコマース \> 本社の設定 \> コマース スケジューラ \> チャネル データベース** の順に移動します。
1. 使用可能な他のチャネル **scXXXXXXXXX** を選択します。
1. アクション ウィンドウで、**完全なデータの同期** を選択します。
1. 配送スケジュールとして **9999** を入力します。
1. **OK** を選択します。
1. **OK** を選択します。

### <a name="test-credit-card-information-to-do-test-purchases"></a>テスト購買を実行するためのクレジット カード情報のテスト

サイトでテスト トランザクションを実行するには、次のテスト クレジット カード情報を使用できます。

- **カード番号:** 4111-1111-1111-1111
- **有効期限:** 10/30
- **カード検証値 (CVV) コード:** 737

> [!IMPORTANT]
> どのような状況でも、テスト サイトで実際のクレジット カード情報は絶対に使用しないでください。

## <a name="next-steps"></a>次のステップ

プロビジョニングと構成の手順が完了したら、サンドボックス環境を使用することができます。 コマース サイト ビルダーの URL を使用して、作成エクスペリエンスに移動します。 コマース サイトの URL を使用して、小売顧客サイト エクスペリエンスに移動します。

Commerce サンドボックス環境のオプション機能を構成するには、[Commerce サンドボックス環境のオプション機能の構成](cpe-optional-features.md) を参照してください。

eコマース ユーザーが eコマース サイトにサインインできるようにするには、Azure Active Directory Business to Consumer (B2C) 経由のサイト認証を有効にするための追加設定が必要である。 詳細については、[B2C テナントを Commerce に 設定する](set-up-b2c-tenant.md)を参照してください。

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>サイトの構成時にサイト ビルダーのチャネル リストが空です

サイト ビルダーにオンライン ストア チャネルが表示されない場合は、上記の [始める前に](#before-you-start) セクションで説明されているように、本社でチャンネルが Commerce Scale Unit に追加されていることを確認します。 また、**既存のコンフィギュレーションの削除** の値を **はい** に設定して **コマース スケジューラの初期化** を実行します。  これらの手順が完了したら、**チャネル データベース** ページ (**小売とコマース \> 本社の設定 \> コマース スケジューラ \> チャネル データベース**) で Commerce Scale Unit に対して **9999** ジョブを実行します。

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>色見本はカテゴリ ページには表示されませんが、製品の詳細ページ (PDP) ページには表示されます

次の手順に従って、色とサイズの見本が調整可能に設定されていることを確認します。

1. 本社で **小売とコマース \> チャンネル設定 \> チャンネル カテゴリと製品属性** に移動します。
1. 左ペインでオンライン ストア チャネルを選択し、**属性メタデータの設定** を選択します。
1. **チャンネルの属性を表示** オプションを **はい** に設定し、**変更可能** オプションを **はい** に設定して、**保存** を選択します。 
1. オンライン ストア チャネル ページに戻り、**チャネル更新の公開** を選択します。
1. **小売とコマース \> 本社の設定 \> コマース スケジューラ \> チャネル データベース** の順に移動し、Commerce Scale Unit で **9999** ジョブを実行します。

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>AdventureWorks ビジネス サイトのビジネス機能が有効になっていないようです

本社で、オンライン ストア チャネルが **B2B** に設定された **顧客タイプ** で構成されていることを確認します。 **顧客タイプ** が **B2C** に設定されている場合、既存のチャンネルは編集できないので新しいチャンネルを作成する必要があります。 

Commerce バージョン 10.0.26 以前に出荷されたデモ データには、**AW Business オンライン ストア** チャンネルが正しく構成されないというバグがありました。 この問題を回避するには、**B2B** に設定する必要がある **顧客タイプ** を除き、同じ設定とコンフィギュレーションで新しいチャンネルを作成します。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce サンドボックス環境のプロビジョニング](provisioning-guide.md)

[Dynamics 365 Commerce サンドボックス環境のオプション機能の構成](cpe-optional-features.md)

[Dynamics 365 Commerce サンドボックス環境での BOPIS の構成](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure ポータル](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce Web サイト](https://aka.ms/Dynamics365CommerceWebsite)

[Commerce での B2C テナントの設定](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

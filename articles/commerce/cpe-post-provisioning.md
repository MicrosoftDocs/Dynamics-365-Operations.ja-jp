---
title: Dynamics 365 Commerce プレビュー環境のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境をプロビジョニング後にコンフィギュレーションする方法について説明します。
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12d3a86698e9250f5d1645de51e0749c8d929f75
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024709"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a>Dynamics 365 Commerce プレビュー環境のコンフィギュレーション


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境をプロビジョニング後にコンフィギュレーションする方法について説明します。

## <a name="overview"></a>概要

このトピックの手順は、Commerce プレビュー環境がプロビジョニングされた後にのみ完了してください。 Commerce プレビュー環境をプロビジョニングする方法については、[Commerce プレビュー環境のプロビジョニング](provisioning-guide.md) を参照してください。

Commerce プレビュー環境をエンドツーエンドでプロビジョニングした後、環境の評価を開始する前に、追加のプロビジョニング後のコンフィギュレーション手順を完了する必要があります。 これらの手順を完了するには、Microsoft Dynamics Lifecycle Services (LCS)、Dynamics 365 Commerce、および Dynamics 365 Retail を使用する必要があります。

## <a name="before-you-start"></a>始める前に

1. [LCS ポータル](https://lcs.dynamics.com) にサインインします。
1. プロジェクトに移動します。
1. トップ メニューで、**クラウド ホスト環境**を選択します。
1. リストで環境を選択します。
1. 右側の環境情報で、**完全な詳細**を選択します。
1. **ログイン**を選択してメニューを開き、**環境にログオン**を選択します。
1. 右上隅にある **USRT** 法人が選択されていることを確認します。

## <a name="configure-the-point-of-sale-in-lcs"></a>LCS での販売時点のコンフィギュレーション

### <a name="associate-a-worker-with-your-identity"></a>作業者と ID の関連付け

LCS で作業者を ID に関連付けるには、次の手順を実行します。

1. 左側のメニューを使用して、**モジュール \> Retail \> 従業員 \> 作業者**の順に移動します。
1. リストで、次のレコードを検索し、選択します: **000713 - アンドリュー コレット**。
1. アクション ウィンドウで、**Retail** を選択します。
1. **既存の ID の関連付け**を選択します。
1. **電子メールを使用した検索**の右にある**電子メール** フィールドに、電子メール アドレスを入力します。
1. **検索** を選択します。
1. 名前を含むレコードを選択します。
1. **OK** を選択します。
1. **保存** を選択します。

### <a name="activate-cloud-pos"></a>クラウド POS の有効化

LCS のクラウド POS を有効にするには、次の手順を実行します。

1. トップ メニューで、**クラウド ホスト環境**を選択します。
1. リストで環境を選択します。
1. 右側の環境情報で、**完全な詳細**を選択します。
1. **ログイン**を選択してメニューを開き、**クラウド販売時点管理にログオンする**を選択して販売時点管理 (POS) を開きます。
1. **次へ** を選択します。
1. Microsoft Azure Active Directory (Azure AD) アカウントを使用してサインインします。
1. **店舗名**で、**サンフランシスコ**を選択します。
1. **次へ** を選択します。
1. **レジスターとデバイス**で、**SANFRAN-1** を選択します。
1. **有効化** を選択します。 サインアウトして、POS のサインイン ページに移動します。
1. オペレーター ID **000713** およびパスワード **123** を使用して、クラウド POS エクスペリエンスにサインインできるようになりました。

## <a name="set-up-your-site-in-commerce"></a>コマースで、サイトを設定します。

コマースでプレビュー サイトの設定を開始するには、次の手順を実行します。

1. プロビジョニング中に E コマースを初期化したときに作成した URL を使用して、サイト管理ツールにサインインします ([E コマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。
1. **Fabrikam** サイトを選択して、サイトの設定ダイアログ ボックスを開きます。
1. E コマースを初期化したときに入力したドメインを選択します。
1. **Fabrikam 拡張オンライン ストア**を既定のチャネルとして選択します。 (**拡張**オンライン ストアが選択されていることを確認してください。)
1. 既定の言語として **en-us** を選択します。
1. **パス** フィールドの値はそのままにしておきます。
1. **OK** を選択します。 サイトでページのリストが表示されます。

## <a name="enable-jobs-in-retail"></a>Retail のジョブの有効化

Retail のジョブを有効化するには、次の手順に従います。

1. 環境 (HQ) にサインインします。
1. 左側のメニューを使用して、**Retail \> 照会およびレポート \> バッチ ジョブ**の順に移動します。

    この手順の残りの部分は、次の各ジョブに対して完了する必要があります。

    * 小売用の注文電子メール通知の処理
    * 製品の使用可能性
    * P-0001
    * 注文ジョブを同期します

1. クイック フィルターを使用して、名前でジョブを検索します。
1. ジョブの状態が**源泉徴収**の場合、次の手順を実行します。

    1. レコードを選択します。
    1. アクション ウィンドウの、**バッチ ジョブ** タブで、**状態の変更**を選択します。
    1. **待機中**を選択し、**OK** を選択します。

### <a name="run-full-data-synchronization-in-retail"></a>Retail で完全なデータ同期の実行

Retail で完全なデータ同期を実行するには、次の手順を実行します。

1. 左側にあるメニューを使用して、**モジュール \> Retail \> 本社の設定 \> 小売用スケジューラ \> チャネル データベース**の順に移動します。
1. 左側のリストで、**既定**のチャネルが選択できます。 使用可能な他のチャンネルを選択します。 このチャンネルは **scXXXXXXXXX** と呼ばれます。
1. アクション ウィンドウで、**完全なデータの同期**を選択します。
1. 配送スケジュールとして **9999** を入力します。
1. **OK** を選択します。
1. **OK** を選択します。

### <a name="test-credit-card-information-to-do-test-purchases"></a>テスト購買を実行するためのクレジット カード情報のテスト

サイトでテスト トランザクションを実行するには、次のテスト クレジット カード情報を使用できます。

- **カード番号:** 4111-1111-1111-1111
- **有効期限:** 10/20
- **カード検証値 (CVV) コード:** 737

> [!IMPORTANT]
> どのような状況でも、テスト サイトで実際のクレジット カード情報は絶対に使用しないでください。

## <a name="next-steps"></a>次のステップ

プロビジョニングとコンフィギュレーションの手順が完了したら、プレビュー環境を評価する準備ができています。 コマース サイト管理ツールの URL を使用して、作成エクスペリエンスに移動します。 コマース サイトの URL を使用して、小売顧客サイト エクスペリエンスに移動します。

Commerce プレビュー環境のオプション機能をコンフィギュレーションするには、[Commerce プレビュー環境のオプション機能のコンフィギュレーション](cpe-optional-features.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce プレビュー環境の概要](cpe-overview.md)

[Dynamics 365 Commerce プレビュー環境のプロビジョニング](provisioning-guide.md)

[Dynamics 365 Commerce プレビュー環境のオプション機能のコンフィギュレーション](cpe-optional-features.md)

[Dynamics 365 Commerce プレビュー環境に関するよく寄せられる質問](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure ポータル](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce Web サイト](https://aka.ms/Dynamics365CommerceWebsite)

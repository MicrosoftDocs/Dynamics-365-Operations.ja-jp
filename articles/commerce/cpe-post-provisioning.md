---
title: Dynamics 365 Commerce の評価環境を構成する
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニング後に構成する方法について説明します。
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413646"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce の評価環境を構成する

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の評価環境をプロビジョニング後に構成する方法について説明します。

## <a name="overview"></a>概要

このトピックに記載の手順は、コマースの評価環境がプロビジョニングされた後でのみ着手してください。 コマースの評価環境をプロビジョニングする方法については、[コマースの評価環境のプロビジョニング](provisioning-guide.md) を参照してください。

コマースの評価環境をエンドツーエンドでプロビジョニングした後は、環境の評価を開始する前に、プロビジョニング後の追加の構成ステップを完了する必要があります。 これらの手順を完了するには、Microsoft Dynamics Lifecycle Services (LCS) と Dynamics 365 Commerce を使用する必要があります。

## <a name="before-you-start"></a>始める前に

1. [LCS ポータル](https://lcs.dynamics.com) にサインインします。
1. プロジェクトに移動します。
1. トップ メニューで、**クラウド ホスト環境** を選択します。
1. リストで環境を選択します。
1. 右側の環境情報で、**環境にログインする** を選択します。 コマースの本部に送信されます。
1. 右上隅にある **USRT** 法人が選択されていることを確認します。

コマース本部でのプロビジョニング後の活動では、法人として **USRT** が常に選択されていることを確認してください。

## <a name="configure-the-point-of-sale"></a>販売時点管理を構成する

### <a name="associate-a-worker-with-your-identity"></a>作業者と ID の関連付け

作業者を ID に関連付けるには、コマース本部で次の手順を実行します。

1. 左側のメニューを使用して、**モジュール \> 小売りとコマース \> 従業員 \> 作業者** の順に移動します。
1. リストで、次のレコードを検索し、選択します: **000713 - アンドリュー コレット**。
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

## <a name="set-up-your-site-in-commerce"></a>コマースで、サイトを設定します。

コマースで評価サイトの設定を開始するには、次の手順を実行します。

1. プロビジョニングの実行時に eコマースを初期化した際に作成した URL を使用して、コマース サイトの管理ツールにサイン インします ([eコマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。
1. **Fabrikam** サイトを選択して、サイトの設定ダイアログ ボックスを開きます。
1. E コマースを初期化したときに入力したドメインを選択します。
1. **Fabrikam 拡張オンライン ストア** を既定のチャネルとして選択します。 (**拡張** オンライン ストアが選択されていることを確認してください。)
1. 既定の言語として **en-us** を選択します。
1. **パス** フィールドの値はそのままにしておきます。
1. **OK** を選択します。 サイトでページのリストが表示されます。

## <a name="enable-jobs"></a>ジョブの有効化

コマースのジョブを有効化するには、次の手順に従います。

1. 環境 (HQ) にサインインします。
1. 左側のメニューを使用して、**小売りとコマース \> 照会およびレポート \> バッチ ジョブ** の順に移動します。

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

必要に応じて、以下のジョブの繰り返し間隔を1分に設定することも可能です。

* 小売用の注文電子メール通知ジョブの処理
* P-0001 ジョブ
* 注文ジョブを同期します

### <a name="run-full-data-synchronization"></a>完全データ同期の実行

コマースで完全なデータ同期を実行するには、コマース本部で次の手順を実行します。

1. 左側のメニューを使用して、**モジュール \> 小売りとコマース \> 本社の設定 \> コマース スケジューラ \> チャネル データベース** の順に移動します。
1. 使用可能な他のチャネル **scXXXXXXXXX** を選択します。
1. アクション ウィンドウで、**完全なデータの同期** を選択します。
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

プロビジョニングと構成の手順が完了したら、評価環境を使用することができます。 コマース サイト ビルダーの URL を使用して、作成エクスペリエンスに移動します。 コマース サイトの URL を使用して、小売顧客サイト エクスペリエンスに移動します。

コマースの評価環境のオプション機能を構成するには、[コマース評価環境のオプション機能を構成する](cpe-optional-features.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce 評価環境の概要](cpe-overview.md)

[Dynamics 365 Commerce 評価環境をプロビジョニングする](provisioning-guide.md)

[Dynamics 365 Commerce 評価環境のオプション機能を構成する](cpe-optional-features.md)

[Dynamics 365 Commerce 評価環境で BOPIS を構成する](cpe-bopis.md)

[Dynamics 365 Commerce 評価環境に関するよく寄せられる質問](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure ポータル](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce Web サイト](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
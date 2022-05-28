---
title: Dynamics 365 Commerce と Microsoft Teams の統合を有効化する
description: このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams の統合を有効化する方法について説明します。
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dfada577ab97fdb9912c22d2399529f934b25d54
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695737"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Dynamics 365 Commerce と Microsoft Teams の統合を有効化する

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams の統合を有効化する方法について説明します。

Teams に Dynamics 365 Commerce からの情報を提供し、Teams と 販売時点管理 (POS) のアプリケーション間でタスク管理機能を同期させるには、Commerce 本部で統合機能を有効にする必要があります。

> [!NOTE]
> Teams の 統合を有効にした場合、Teams とデータを共有することに同意することになります。 Teams と共有するデータは、ご利用の Commerce データとは異なる国に存在する可能性があり、また、異なるコンプライアンス基準の対象となる可能性があります。 詳細については、[Microsoft トラストセンター](https://www.microsoft.com/trust-center) を参照してください。 マイクロソフトのプライバシー ポリシーについては、 [Microsoft プライバシー ステートメント](https://aka.ms/privacy)を参照してください。

## <a name="enable-teams-integration"></a>Teams との統合を有効化する

Microsoft Teams と Commerce との統合を有効にする前に、Azure ポータルで Teams アプリケーションをテナントに登録する必要があります。

Azure ポータルで Teams アプリケーションをテナントに登録するには、以下の手順に従います。

1. [クイック スタート : Microsoft IDプラットフォームにアプリを登録する](/azure/active-directory/develop/quickstart-register-app) に記載の手順に従い、Azure ポータルで Teams アプリケーションをテナントに登録します。
1. **アプリの登録** タブで、前述の手順で作成したアプリを選択します。 **認証** タブで、**プラットフォームの追加** を選択します。
1. ダイアログ ボックスで、**Web** を選択します。 **リダイレクト URL** フィールドで、**\<HQUrl\>/oauth** の形式で URL を入力します。 **\<HQUrl\>** をご利用の Commerce 本部の URL に置き換えます (例: `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`)。
1. 登録したアプリの **概要** ページで、**アプリケーション (クライアント) ID** をコピーします。 次のセクションで Commerce 本部での Teams 統合を有効にするために、この値を提供する必要があります。
1. [クライアント シークレットの追加](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret)の手順に従って、クライアント シークレットを追加します。 続いて、クライアント用の **シークレットの値** をコピーします。 次のセクションで Commerce 本部での Teams 統合を有効にするために、この値を提供する必要があります。
1. **API のアクセス許可**、**アクセス許可の追加** の順に選択します。
1. **API 権限の要求** ダイアログ ボックスで、 **Microsoft Graph** を選択して **委任されたアクセス許可** を選択し、**グループ** を展開して、**Group.ReadWrite.All** を選択して **アクセス許可の追加** を選択します。
1. **API 権限の要求** ダイアログ ボックスで、 **アクセス許可の追加** を選択して **Microsoft Graph** を選択し、**アプリケーションのアクセス許可** を選択して **グループ** を展開して、**Group.ReadWrite.All** を選択して **アクセス許可の追加** を選択します。
1. **API 権限の要求** ダイアログ ボックスで、**アクセス許可の追加** を選択します。 **組織が使用している API** タブで、**Microsoft Teams 小売りサービス** を検索し、選択します。
1. **委任されたアクセス許可** を選択し、**TaskPublishing** を展開し、**TaskPublising.ReadWrite.All** を展開して **アクセス許可の追加** を選択します。 詳細については、[Web API にアクセスするクライアント アプリケーションを構成する](/azure/active-directory/develop/quickstart-configure-app-access-web-apis) を参照してください。

Commerce 本部で Teams の統合を有効にするには、以下の手順に従います。

1. **小売とコマース \> チャネル設定 \> Microsoft Teams 統合の構成** に移動します。
1. アクション ウィンドウで、**編集** を選択します。
1. **有効化 Microsoft Teams 統合** オプションを **はい** に設定します。
1. **アプリケーション ID** フィールドで、Azure ポータルで Teams アプリケーションを登録した際に取得した **アプリケーション (クライアント) ID** 値を入力します。
1. **アプリケーション キー** フィールドで、Azure ポータルでクライアント シークレットを追加した際に取得した **シークレット値** を入力します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、Commerce 本部での Teams 統合の設定例です。

![Commerce 本部の Teams 統合構成。](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Teams との統合を無効化する

Commerce 本部で Microsoft Teams の統合を無効にするには、以下の手順に従います。

1. **小売とコマース \> チャネル設定 \> Microsoft Teams 統合の構成** に移動します。
1. アクション ウィンドウで、**編集** を選択します。
3. **有効化 Microsoft Teams 統合** オプションを **いいえ** に設定します。
4. **アプリケーションID** フィールドと **アプリケーション キー** フィールドから値をクリアします。
1. アクション ウィンドウで、**保存** を選択します。

> [!NOTE]
> Commerce と Teams の統合を無効にすると、POS 端末には Teams アプリケーションから発行されたタスクが表示されなくなります。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce と Microsoft Teams データ統合の概要](commerce-teams-integration.md)

[Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング](provision-teams-from-commerce.md)

[Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる](synchronize-tasks-teams-pos.md)

[Microsoft Teams でユーザーとロールを管理する](manage-user-roles-teams.md)

[Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします](map-stores-existing-teams.md)

[Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ](teams-integration-faq.md)

---
title: サービス間認証の構成
description: このトピックでは、評価とレビューのためにサービス API を安全に呼び出すように Microsoft Dynamics 365 Commerce でサービス間認証を構成する方法について説明します。
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: da780de5f15d72bdac85a261eae809125c830260
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968521"
---
# <a name="configure-service-to-service-authentication"></a>サービス間認証の構成

[!include [banner](includes/banner.md)]

このトピックでは、評価とレビューのために サービス アプリケーション プログラミング インターフェイス (API) を安全に呼び出すように Microsoft Dynamics 365 Commerce でサービス間 (S2S) 認証を構成する方法について説明します。

Dynamics 365 Commerce は、オムニチャネル ソリューションとして、[評価とレビュー](ratings-reviews-overview.md)を提供しています。 このソリューションにより、Commerce の外部からサービス API にアクセスして、さまざまなタスクを実行できます。 これらのタスクには、外部システムから Commerce への評価とレビューのインポート、および Commerce からの評価とレビューのエクスポートが含まれます。 Commerce が評価とレビューのサービス API を安全に呼び出すことができるようにするには、まずこのトピックの手順に従ってS2S 認証を構成する必要があります。

## <a name="add-a-new-app-registration"></a>新しいアプリ登録の追加

新しいアプリの登録を追加する前に、[Azure ポータル](https://portal.azure.com) を使用してアプリケーションを作成する必要があります。 Azure Active Directory (Azure AD) にアプリを登録し認証を有効にするには、[Azure Active Directory を Power Automate のカスタム コネクタで使用](/connectors/custom-connectors/azure-active-directory-authentication) の手順に従います。

次の ID を Azure ポータルから取得します。 これらの ID は、次の手順で必要になります。

- クライアント アプリケーション ID
- クライアント ディレクトリ (テナント) ID

Commerce サイト ビルダーで新しいアプリ登録を追加するには、次の手順に従います。

1. **ホーム \> レビュー \> 設定** に移動します。
1. **サービス間 (S2S) 認証** で、**管理** を選択します。

    ![Commerce サイト ビルダーのサービス間 (S2S) 認証セクションの管理ボタン。](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. 右側に表示される **S2S アプリ エントリ** ペインで、**新しい S2S アプリ登録の追加** を選択します。
1. **S2S アプリ エントリの追加** ダイアログ ボックスで、次の必要な情報を入力します。 Azure アプリケーションの登録からの値を使用します。

    - **名前** – アプリケーションの名前を入力します (例えば **Fabrikam アプリ**)。
    - **クライアント アプリ ID** – アプリケーション ID を入力します (例えば **00000000-0000-0000-0000-000000000000**)。
    - **ディレクトリ (テナント) ID** – ディレクトリ ID を入力します (例えば **00000000-0000-0000-0000-000000000000**)。

    ![Commerce サイト ビルダーの S2S アプリ エントリの追加ダイアログ ボックス。](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. **送信** を選択します。 アプリケーションの名前が、**S2S アプリ エントリ** ペインの一覧に表示されます。
1. **S2S アプリ エントリ** ペインを閉じます。
1. **保存** を選択します。

## <a name="edit-an-existing-app-registration"></a>既存のアプリ登録の編集

Commerce サイト ビルダーで既存のアプリ登録を編集するには、次の手順に従います。

1. **ホーム \> レビュー \> 設定** に移動します。
1. **サービス間 (S2S) 認証** で、**管理** を選択します。
1. **S2S アプリ エントリ** ペインで、編集するエントリの横にある鉛筆アイコンを選択します。
1. 必要に応じて **名前**、**クライアント アプリ ID**、**ディレクトリ (テナント) ID** のフィールドの値を更新します。
1. **送信** を選択します。
1. **S2S アプリ エントリ** ペインを閉じます。
1. **保存** を選択します。

## <a name="remove-an-existing-app-registration"></a>既存のアプリ登録の削除

Commerce サイト ビルダーで既存のアプリ登録を削除するには、次の手順に従います。

1. **ホーム \> レビュー \> 設定** に移動します。
1. **サービス間 (S2S) 認証** で、**管理** を選択します。
1. **S2S アプリ エントリ** ペインで、削除するエントリの横にあるごみ箱アイコンを選択します。 このエントリは一覧から削除されます。
1. **S2S アプリ エントリ** ペインを閉じます。
1. **保存** を選択します。

## <a name="additional-resources"></a>追加リソース

[評価とレビューの概要](ratings-reviews-overview.md)

[評価とレビューを使用するためのオプト イン](opt-in-ratings-reviews.md)

[評価とレビューの管理](manage-reviews.md)

[評価とレビューの構成](configure-ratings-reviews.md)

[製品評価の同期](sync-product-ratings.md)

[モデレーターによる評価とレビューの手動公開を有効にする](manual-publish-rating-reviews.md)

[評価とレビューのインポートとエクスポート](import-export-reviews.md)

[評価とレビューに関するよく寄せられる質問](ratings-reviews-faq.md) 

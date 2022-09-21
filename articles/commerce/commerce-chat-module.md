---
title: Customer Service 用オムニチャネルを使った Commerce チャット モジュール
description: この記事では、Microsoft Dynamics 365 Commerce で Customer Service 用オムニチャネルを使った Commerce チャットについて説明します。
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: b8eaed3eb015e96b1db6fa2297c341ea9d3ff8ad
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473812"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Customer Service 用オムニチャネルを使った Commerce チャット モジュール

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce での *Customer Service 用オムニチャネル* を使った Commerce チャット モジュールについて説明します。

Commerce Version 10.0.29 リリースでは、Customer モジュール ライブラリに新しい Customer Service 用オムニチャネルを使った Commerce チャットが追加されています。 この Commerce チャット機能は、Dynamics 365 の Customer Service 用オムニチャネルのチャット機能を e コマース顧客に提供します。このサービスには、顧客のクエリへの対処、顧客サービスの提供、Commerce 顧客への販売の容易化を支援するライブ チャット オペレーターのサポートが含まれています。

この Commerce チャット機能は、小売業者が次なる目標を達成できるようにします。

- 顧客維持を向上させるために、顧客とのカスタマイズされた関与を増やします。
- 人間のエージェントとセルフサービスのチャットボットを統合して、顧客サービスを改善します。
- 運用上の改善と関与を促進するリアルタイムの顧客プロファイル、注文、購買データを利用することで、ヘルプ担当者が経験を得るのを支援します。
- 販売の向上に役立つ、全体的な顧客満足の向上。

次の機能は、Commerce チャット機能の一部として使用できます。

- Customer Service 用オムニチャネルを使った Commerce チャット
- Dynamics 365 の Customer Service 用オムニチャネルでのエージェント体験での、アプリケーション タブとしての **Commerce コール センター** の追加

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Customer Service 用オムニチャネルの前提条件

前提条件として、Customer Service 用オムニチャネルの管理ウィジェットでチャットを構成して、いくつかのパラメータを取得して Commerce のチャット体験を構成する必要があります。 手順については、[チャット チャネルの構成](/dynamics365/customer-service/set-up-chat-widget) を参照してください。

Customer Service 用オムニチャネルの管理ウィジェットでチャットを構成した後、次のようなスクリプトが表示されます。

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

このスクリプトをコピーします。チャット モジュールを構成するにはここに値があることが必要です。

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Customer Service 用オムニチャネルを使った Commerce チャットの必須フィールド

次の表は、Customer Service 用オムニチャネルを使った Commerce チャットモジュールを構成するのに必要な、Customer Service 用オムニチャネルの管理ウィジェットからのスクリプト値を表示しています。

| ウィジェット プロパティ | Description |
| ------------- |--------------|
| スクリプト ソース | チャット ウィジェット スクリプトの **src** の値。 |
| データ申請 ID | チャット ウィジェット スクリプトの **data-app-id** の値。 |
| データ組織 ID | チャット ウィジェット スクリプトの **data-org-id** の値。 |
| データ組織 URL | チャット ウィジェット スクリプトの **data-org-url** の値。 |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>e コマース サイト用に Commerce チャット体験を構成する

e コマース サイトでチャット体験使用するための推奨される 1 つの方法は、e コマース サイト ページで使用する共有ヘッダーのフラグメントに、Customer Service 用オムニチャネルを使った Commerce チャットを追加することです。

Commerce サイト ビルダーの自分のサイトのヘッダー フラグメントにチャット モジュールを追加するには、以下の手順に従います。

1. 自分のサイトのサイトビルダーで、**フラグメント** に移動します。
1. **新規** を選択します。
1. **フラグメントの選択** ダイアログ ボックスで、**Customer Service 用オムニチャネルを使った Commerce チャット** モジュールでフラグメントの名前を入力して、**OK** を選択します。
1. 概要ビューで、**Msd msd365 cs のコネクタ** スロットを選択します。
1. 右側の **チャット プロパティ** ウィンドウで、次のステップに従います。

    1. **スクリプト ソース** フィールドに、Customer Service 用オムニチャネルから取得した **src** 値を入力します。
    1. **データ スクリプト ID** フィールドに、Customer Service 用オムニチャネルから取得した **data-app-id** 値を入力します。
    1. **データ組織 ID** フィールドに、Customer Service 用オムニチャネルから取得した **data-org-id** 値を入力します。
    1. **データ組織 URL** フィールドに、Customer Service 用オムニチャネルから取得した **data-org-url** 値を入力します。

    ![Commerce サイト ビルダーで Commerce チャット モジュールのフラグメントを作成する](media/Commerce-chat-creating-new-fragment.png)

1. **保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。
1. **フラグメント** に移動し、自分のサイトのヘッダー フラグメントを開きます。
1. **既定のコンテナー** スロットで、省略ボタン (**...**) を選択し、**フラグメントの追加** を選択します。
1. **モジュールの選択** ダイアログ ボックスで、以前に作成したチャット フラグメントを選択し、**OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Customer Service 用オムニチャネルのアプリケーション タブとして Commerce Headquarters を追加する

Customer Service 用オムニチャネルの Commerce Headquarters 向けにアプリケーション タブを追加できます。 その後、ライブ チャット オペレーターは、Customer Service 用オムニチャネルのユーザー インターフェイスを使用して、顧客のコンテキスト情報を販売注文情報と共に含んだ Dynamics 365 Commerce 顧客サービス モジュールに簡単にアクセスできます。 さらに、顧客サービス担当者は、新しい注文を行い、返品を開始し、注文のステータス情報を確認できます。

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>iFrame モジュールに Commerce Headquarters を読み込む新しいアプリケーション タブの 作成 

iFrame モジュールに Commerce Headquarters を読み込む新しいアプリケーション タブを作成するには、これらの手順に従ってください。

1. [Power Apps Maker Portal](https://make.powerapps.com) を開きます。
1. 左のナビゲーション ウィンドウで、**アプリ** を選択します。
1. **顧客サービス管理センター** を選択します。
1. **エージェント体験** に移動します。
1. **アプリケーション テンプレート** に対しては、**管理** を選択します。
1. **サード パーティ Web サイト** タイプの新しいアプリケーション タブを作成します。 手順については、[アプリケーション タブのテンプレートを管理する](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter) をご覧ください。
1. **パラメーター** の、**URL** パラメータの **値** フィールドで、次の URL を入力します。ここで `<YourOrganizationHeadquartersURL>` と `<LegalEntityname>` は適切な値に置き換えられる場所を指定します。 Customer Service 用オムニチャネルは、チャット コンテキストから **{AccountNumber}** を読み取ります。 したがって、そのまま **{AccountNumber}** を残します。

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. **データ** パラメータ の **値** フィールドは空白のままにします。

![Dynamics 365 のCustomer Service 用オムニチャネルのアプリケーション タブの作成](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Dynamics 365の Customer Service 用オムニチャネルの新しいアプリケーション タブを有効にする

Dynamics 365の Customer Service 用オムニチャネルで顧客エージェントに対して新しいアプリケーション タブを有効にするには、次の手順に従います。
    
1. [Power Apps Maker Portal](https://make.powerapps.com) を開きます。
1. 左のナビゲーション ウィンドウで、**アプリ** を選択します。
1. **顧客サービス管理センター** を選択します。
1. **カスタマー サポート \> ワークストリーム** に移動します。
1. エージェントに対して作成したワーク ストリームを開き、**詳細設定** で **セッションの既定値** を選択します。
1. **アプリケーション タブ** で、**既存のアプリケーション タブの追加** を選択し、上で作成した新しいアプリケーション タブを追加します。 この手順により、エージェントが e コマース Webサイトから着信する電話を受けるときに iFrame モジュールに Commerce Headquarters を読み込むアプリケーション タブが表示されます。

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Dynamics 365 の Customer Service 用オムニチャネルでコンテキスト変数を追加する

Dynamics 365 の Customer Service 用オムニチャネルでコンテキスト変数を追加するには、次の手順に従います。

1. [Power Apps Maker Portal](https://make.powerapps.com) を開きます。
1. 左のナビゲーション ウィンドウで、**アプリ** を選択します。
1. **顧客サービス管理センター** を選択します。
1. **カスタマー サポート \> ワークストリーム** に移動します。
1. エージェントに対して作成したワーク ストリームを開き、**詳細設定** で **コンテキスト変数** セクションに移動します。
1. **編集** を選択し、**AccountNumber** を **テキスト** タイプのコンテキスト変数として追加します。 この変数は、Commerce Headquarters が一致する勘定番号を使用して顧客情報を読み込むのに役立ちます。

> [!NOTE]
> メールアドレスと e コマース チャンネルからサインイン ユーザーの名前を読み込む場合は、**AccountNumber** コンテキスト変数への追加に加えて、**メール** と **名前** を **テキスト** タイプのコンテキスト変数として追加できます。

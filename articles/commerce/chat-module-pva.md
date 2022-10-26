---
title: Power Virtual Agents を使った Commerce チャット モジュール
description: この記事では、Microsoft Power Virtual Agents を Dynamics 365 Commerce Webサイトと統合する Power Virtual Agents を使った Commerce チャット モジュールについて説明します。
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691084"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Power Virtual Agents を使った Commerce チャット モジュール

[!include [banner](includes/banner.md)]

この記事では、Microsoft Power Virtual Agents を Dynamics 365 Commerce Webサイトと統合する Power Virtual Agents を使った Commerce チャット モジュールについて説明します。

Power Virtual Agents を使った Commerce チャット機能は、Dynamics 365 e Commerce 顧客がクエリを処理するために Power Virtual Agents チャットボット機能を使用できる機能です。 Dynamics 365 Commerce 10.0.30 リリース時点で、この機能は、Commerce モジュール ライブラリの一部である Power Virtual Agents を使った Commerce チャット モジュールを使用することで eコマース web サイトに組み込むことができます。

Power Virtual Agents を使った Commerce チャット機能は、企業が次の目標を達成するのに役立ちます。

- 顧客維持を向上させるために、顧客とのカスタマイズされた関与を増やします。
- セルフサービスのチャットボットを統合して、顧客サービスを向上させます。
- 全体的な顧客満足を向上させ、結果として販売が向上します。

> [!NOTE]
> Dynamics 365 Customer Service 用オムニチャネル と Power Virtual Agents アプリケーションとの間の違いについては、[Commerce チャット モジュールの概要](/commerce-chat-modules-overview.md) を参照してください。

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>Power Virtual Agents を使用するための前提条件

Power Virtual Agents 機能を使った Commerce チャットを使用するには、最初に e コマース Webサイト用に Power Virtual Agents チャットボットを作成する必要があります。 手順については、[Power Virtual Agent ボットの作成](/power-virtual-agents/authoring-first-bot) を参照してください。

これらのオブジェクト グループを設定した後、Commerce チャットを構成するために、**ボット ID** と **テナント ID** の値をコピーする必要があります。 これらの値をコピーする方法の詳細については、[Power Virtual Agents ボット パラメーターの取得](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters) を参照してください。

## <a name="configure-your-e-commerce-site"></a>e-コマース サイトの構成 

e コマース サイトでチャット体験使用するための推奨される 1 つの方法は、サイト ページで使用する共有ヘッダーのフラグメントに、Power Virtual Agents を使った Commerce チャット モジュールを追加することです。

Commerce サイト ビルダーの自分のサイトのヘッダー フラグメントにチャット モジュールを追加するには、以下の手順に従います。

1. 自分のサイトのサイトビルダーで、**フラグメント** に移動します。
1. **新規** を選択します。
1. **フラグメントの選択** ダイアログ ボックスで、**Power Virtual Agents を使った Commerce チャット** モジュールでフラグメントの名前を入力して、**OK** を選択します。
1. 概要ビューで、**Msdyn365 pva チャット コネクタ** スロットを選択します。
1. 右側の チャット プロパティ ウィンドウで、次のステップに従います。

    1. **ボット パラメータ** の下にある **Bot Framework Webchat Chat CDN URL** フィールドは、既定値 (たとえば `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`) のままにします。
    1. **Bot Framework Direct Line 認証 URL** フィールドは、規定値 (例えば、`https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`) のままにします。
    1. **ボット ID** フィールドで、[Power Virtual Agents を使用するための前提条件](#prereq)でコピーした Power Virtual Agents **ボット ID** 値を入力します。
    1. **テナント ID** フィールド に、コピーした **テナントID** の値を入力します。

1. **保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。
1. **フラグメント** に移動し、自分のサイトのヘッダー フラグメントを開きます。
1. **既定のコンテナー** スロットで、省略ボタン (**...**) を選択し、**フラグメントの追加** を選択します。
1. **モジュールの選択** ダイアログ ボックスで、以前に作成したチャット フラグメントを選択し、**OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してフラグメントにチェックインし、**発行** を選択して公開します。

## <a name="proactive-chat-parameters"></a>プロアクティブなチャット パラメーター

プロアクティブなチャット構成パラメータの完全な一覧については、[Commerce チャット モジュールのプロアクティブなチャット パラメータ](chat-proactive-chat-parameters.md) を参照してください。

> [!NOTE]
> 現在、Power Virtual Agents は Azure Active Directory B2C (Azure AD B2C) 認証をサポートしていません。 製品の入手可能性を得る、または他の匿名 API と対話するために匿名 Retail Cloud Scale Unit (RCSU) 呼び出しのみをサポートします。 Power Virtual Agents チャットボットを介した認証済 API への呼び出しには、明示的な顧客サインインが必要です。

## <a name="additional-resources"></a>追加リソース

[Commerce チャット機能の概要](commerce-chat-overview.md)

[Customer Service 用オムニチャネルを使った Commerce チャット モジュール](commerce-chat-module.md)

[Commerce チャット モジュールのプロアクティブなチャット パラメータ](chat-proactive-chat-parameters.md)

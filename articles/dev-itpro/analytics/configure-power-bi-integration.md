---
title: "ワークスペースの Power BI 統合のコンフィギュレーション"
description: "このトピックでは、PowerBI.com との統合をサポートする 新しい Microsoft Dynamics 365 for Finance and Operations 環境をコンフィギュレーションする方法について説明します。 このコンフィギュレーションにより、ワークスペースに Power BI コントロールが表示され、ユーザーはワークスペースに視覚エフェクトをピン留めすることができます。"
author: MilindaV2
manager: AnnBe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PowerBIConfiguration
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 27661
ms.assetid: 861cfa94-c6f3-4c84-89ac-22c78bf6b7a4
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d540d8093743073aa61bd3c7ab3b66dbedd35b03
ms.openlocfilehash: 15d259d26ece872925290b64c0d7e17063cb1524
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2018

---

# <a name="configure-power-bi-integration-for-workspaces"></a>ワークスペースの Power BI 統合のコンフィギュレーション

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>概要

Microsoft Dynamics 365 for Finance and Operations で、ユーザーは自分の PowerBI.com アカウントからワークスペースにタイル、ダッシュボード、レポートをピン留めできます。

この機能を使用するには、構成を一度設定する必要があります。 管理者は、Finance and Operations および Microsoft Power BI が正しく通信し認証するためにこの手順を実行する必要があります。

Finance and Operations と PowerBI.com の両方はクラウドベースのサービスです。 Power BI タイルを表示するための Finance and Operations ワークスペースでは、Finance and Operations のサーバーはユーザーの代理として Power BI サービスに連絡し視覚化にアクセスする必要があります。 そして、Finance and Operations ワークスペースで視覚化を再描画する必要があります。 Finance and Operations サーバーが Power BI サービスに「ユーザーの代わりに」連絡するという事実は重要です。 `D365User@contoso.com` などのユーザーが BI PowerBI.com サービスに連絡すると、Power BI は、ユーザーの独自の PowerBI.com サブスクリプションからタイルとレポートのみを表示するはずです。

この構成ステップが完了すると、Finance and Operations が PowerBI.com サービスに連絡できるようになります。

## <a name="things-you-must-know-before-you-start"></a>開始前に知っておく必要事項 

- Finance and Operations のシステム管理者である必要があります。 このオプションは、**システム管理**メニューで利用できます。
- PowerBI.com のアカウントが必要です。 アカウントを持っていない場合は、試用版アカウントを作成することができます。 (プロ ライセンスは、この構成ステップでは必要ありません。)
- ご自分の Power BI アカウントに、少なくとも 1 つのダッシュボードと 1 つのレポートがあることが必要です。 この構成ステップでは、ダッシュボードやレポートは必要ではありませんが、PowerBI.com アカウントにコンテンツが含まれていない場合コンフィギュレーションを検証することができないかもしれません。
- Microsoft Azure Active Directory (Azure AD) アカウントの管理者である必要があります。 管理者ではない場合は、管理者ユーザーはこのコンフィギュレーションの手順をユーザーのために実行する必要があります。
- Finance and Operations に構成されている Azure AD ドメインは、PowerBI.com アカウントに使用したのと同じドメインにする必要があります。 たとえば、Contoso.com ドメイン内で Finance and Operations をプロビジョニングした場合、そのドメインで `Tim@ContosoAX7.onmicrosoft.com` などの Power BI 勘定を持っている必要があります。

## <a name="registration-process"></a>登録プロセス 

1. Azure テナント管理者アカウントを使用して https://portal.azure.com/ にログインします。<br>
> [!NOTE]
> この手順を完了したユーザーは、アプリケーションを登録するテナントの管理者権限を持っている必要があります。

2. **Azure Active Directory** > **アプリケーション登録** > **新しいアプリケーション登録** に移動します。<br>
    ![Azure ポータル アプリケーションの登録](media/Azure-Portal-AppRegistration.png)

3. 次の値を入力します。

- **名前** - アプリの名前。
- **アプリケーション タイプ** - Web アプリ/API
- **サインオン URL** - Finance and Operations クライアントと OAuth 接尾語のベース URL。 たとえば、http://contosoax7.cloud.dynamics.com/oauth。
             
4. **作成** をクリックします。
5. **アプリケーション ID** をコピーします。 これは、PowerBI.com サービスに接続するために Finance and Operations で使用されます。
6. **設定** > **必要なアクセス許可** > **追加** > **API の選択** > **Power BI サービス (Power BI)** をクリックします。
7. **選択** をクリックします。
8. アクセスを有効にして **選択** をクリックします。<br>
    ![Azure ポータル アプリのアクセス許可](media/Azure-Portal-AppPermissions.png)

9. **完了** をクリックし、**アクセス許可の付与** をクリックします。
10. **設定** > **キー** をクリックします。
11. **キーの説明** および **期限切れ日時** に値を入力し、**保存** をクリックします。

**アプリケーション ID** および **アプリケーション キー** を書き留めます。 次の手順で、これらの値を使用します。

## <a name="specify-power-bi-settings-in-finance-and-operations"></a>Finance and Operations で Power BI 設定を指定

1. Finance and Operations クライアントで **Power BI コンフィギュレーション** ページを開きます。<br>
    ![Power BI コンフィギュレーション ダイアログ](./media/D365-PBI-Configuration.png)

2. **編集**を選択します。
3. **有効** オプションを **はい** に設定します。
4. **アプリケーション ID** フィールドで、前の手順で Power BI から取得した**アプリケーション ID** の値を入力します。
5. **アプリケーション キー** フィールドで、前の手順で Power BI から取得した**アプリケーション キー**の値を入力します。

    Power BI のコンテンツに **会社** という名前のテーブルおよび **ID** という名前の列がある場合にのみ、会社のフィルターを適用することができます。 Finance and Operations によってリリースされた既存の Power BI コンテンツは、この会話を使用します。

6. **保存** をクリックします。

次のセクションの手順を実行して変更を確認し、PowerBI.com の統合を有効にします。

## <a name="pin-tiles-to-a-workspace"></a>ワークスペースにタイルを固定

1. PowerBI.com コンフィギュレーションを検証するには、**開始する** をクリックします。<br>
> [!NOTE]
> 変更を適用するにはブラウザーを更新する必要があります。 <br>
> ![Power BI の承認](./media/D365-PBI-GetStarted.png)

Finance and Operations の Power BI をはじめて使用する場合は、Finance and Operations クライアントから Power BI へのサインインを承認するように求められます。 **ここをクリックして Power BI に承認を与える** を選択します。

ユーザーは、初めて Power BI コンテンツをピン留めするとき、このステップを完了する必要があります。

2. Azure AD の同意ページは、お客様の同意を求めます。 Finance and Operations がユーザーに代わって PowerBI.com にアクセスするには、ユーザーの同意が必要です。 **受け入れる** を選択します。

3. Finance and Operations の Azure AD に既にサインインしているので、再度資格情報を入力する必要はありません。 新しいタブが表示され、Finance and Operations と Power BI の間の接続を承認するように求められます。 接続を承認し元のタブに戻ります。

4. PowerBI.com アカウントのタイルの一覧が表示されます。 1 つまたは複数のタイルを選択し、選択したワークスペースにピン留めします。
    ![Power BI 統合の検証](./media/D365-PBI-Validation.png)

## <a name="troubleshooting-common-errors"></a>一般的なエラーのトラブルシューティング

上の手順で **承諾** をクリックした後、プロセスが失敗した場合、次のエラー メッセージが表示される場合があります。 エラーの詳細がメッセージの下部に表示されていることに注意します。 追加の技術情報は、原因を特定するのに役立つヒントを提供します。

### <a name="some-common-issues-and-the-resolution-steps"></a>一般的な問題および解決手順

| エラー                                                       | 解像度 |
|-------------------------------------------------------------|------------|
| Power BI サービスは利用できません。                        | この問題は頻繁には発生しませんが、Power BI サービスに到達できないことがあります。 再登録する必要はありません。 後でタイルをワークスペースに固定してみてください。 |
| アプリケーションにアクセスすることはできません。                           | 登録プロセス中に、**手順 3 アクセスする API** の下のすべてのチェック ボックスが選択されなかった可能性があります。 Power BI を起動し、登録プロセスを再実行します。 |
| Power BI タイル ページは空です (コンテンツは表示されません)。     | PowerBI.com アカウントに、ダッシュ ボードまたはタイルがない可能性があります。 サンプル ダッシュ ボードなどのダッシュボードを追加して、もう一度をタイルをピン留めしてみてください。 |
| Power BI を許可する際のエラー                             | Azure 管理者ダッシュボードの、**ユーザーおよびグループ \> ユーザー設定** の下で、**ユーザーはアプリが会社のデータにアクセスすることに同意できる** オプションが **はい** に設定されていることを確認します。 |



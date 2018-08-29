---
title: "ワークスペースの Power BI 統合のコンフィギュレーション"
description: "このチュートリアルでは、新しい Microsoft Dynamics 365 for Finance and Operations、また PowerBI.com との統合をサポートする環境をコンフィギュレーションする方法について説明します。 このコンフィギュレーションにより、ワークスペースに Power BI コントロールが表示され、ユーザーはワークスペースに視覚エフェクトをピン留めすることができます。"
author: MilindaV2
manager: AnnBe
ms.date: 01/09/2018
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f85e9af8aafc0ebd20a93d6a712dbd7b0bf31639
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="configure-power-bi-integration-for-workspaces"></a>ワークスペースの Power BI 統合のコンフィギュレーション

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>概要

Microsoft Dynamics 365 for Finance and Operations で、ユーザーは自分の PowerBI.com アカウントからワークスペースにタイルおよびレポートをピン留めできます。

この機能を使用するには、構成を一度設定する必要があります。 管理者は、Finance and Operations および Microsoft Power BI が正しく通信し認証するためにこの手順を実行する必要があります。

Finance and Operations と PowerBI.com の両方はクラウドベースのサービスです。 Power BI タイルを表示するための Finance and Operations ワークスペースでは、Finance and Operations のサーバーはユーザーの代理として Power BI サービスに連絡し視覚化にアクセスする必要があります。 そして、Finance and Operations ワークスペースで視覚化を再描画する必要があります。 Finance and Operations サーバーが Power BI サービスに「ユーザーの代わりに」連絡するという事実は重要です。 `Tim@ContosoAX7.onmicrosoft.com` などのユーザーが BI PowerBI.com サービスに連絡すると、Power BI は、Tim の独自の PowerBI.com アカウントからタイルとレポートのみを表示するはずです。

この構成ステップが完了すると、Finance and Operations がユーザーの代理で PowerBI.com サービスに連絡できるようになります。 Finance and Operations と Power BI サービス間のフローは、このトピックの後半で説明する OAuth 2.0 Authorization Code Grant Flow に基づいています。

## <a name="things-you-must-know-before-you-start"></a>開始前に知っておく必要事項 

- Finance and Operations のシステム管理者である必要があります。 このオプションは、**システム管理**メニューで利用できます。
- PowerBI.com のアカウントが必要です。 アカウントを持っていない場合は、試用版アカウントを作成することができます。 (プロ ライセンスは、この構成ステップでは必要ありません。)
- ご自分の Power BI アカウントに、少なくとも 1 つのダッシュボードと 1 つのレポートがあることが必要です。 この構成ステップでは、ダッシュボードやレポートは必要ではありませんが、PowerBI.com アカウントにコンテンツが含まれていない場合コンフィギュレーションを検証することができないかもしれません。
- Microsoft Azure Active Directory (Azure AD) アカウントの管理者である必要があります。 管理者ではない場合は、管理者ユーザーはこのコンフィギュレーションの手順をユーザーのために実行する必要があります。
- Finance and Operations に構成されている Azure AD ドメインは、PowerBI.com アカウントに使用したのと同じドメインにする必要があります。 例については、Contoso.com ドメイン内で Finance and Operations をプロビジョニングした場合、そのドメインで `Tim@ContosoAX7.onmicrosoft.com` などの Power BI 勘定を持っている必要があります。

## <a name="registration-process"></a>登録プロセス 

1. 新しいブラウザー セッションを開いて、Power BI アプリ登録を [https://dev.powerbi.com/apps](https://dev.powerbi.com/apps) で開始します。 次の図のようなページが表示されます。

    ![Power BI ページのアプリケーションを登録](./media/PowerBI-registration1.JPG)

2. **既存のアカウントでサインイン** を選択します。 Finance and Operations で使用しているものと同じ Azure AD アカウントを使用して、ブラウザーでサインインしたことを確認します。 サインインの後に、ユーザーの名前は、ページに表示する必要があります。

    ![サインイン後にページに表示されるユーザー名](./media/PowerBI-registration2.JPG)

3. **アプリ名**フィールドで、**Contoso Dyn365 for Operations** などの名前を入力します。
4. **リダイレクト URL** フィールドで、Finance and Operations クライアントのベース URL をコピーして貼り付けてから OAuth の添え字を追加します。 次に例を示します: `http://contosoax7.cloud.dynamics.com/oauth`
5. **ホーム ページの URL** フィールドに、ホーム ページの URL を入力し、モック拡張を追加します。 次に例を示します: `http://contosoax7.cloud.dynamics.com/testenv/`

    この値は必須ですが、ワークスペースの統合には必要ありません。 アプリ ID URI がモック URL であることを確認します。 展開の実際の URL を使用すると、Microsoft Excel アドインなど他の Azure AD アプリケーションでサインインの問題が発生することがあります。 次に例を示します: `http://contosoax7.cloud.dynamics.com/testenv/`

6. **手順 3 アクセスする API を選択** で、すべてのチェック ボックスをオンにします。
7. **アプリの登録** を選択します。
8. **クライアント ID** および**クライアント シークレット** フィールドの値をメモしておきます。 次の手順で、これらの値を使用します。

    ![クライアント ID とクライアント シークレット フィールド](./media/PowerBI-registration3.JPG)

## <a name="specify-power-bi-settings-in-finance-and-operations"></a>Finance and Operations で Power BI 設定を指定

1. Finance and Operations クライアントで **Power BI コンフィギュレーション** ページを開きます。

    ![編集前の Power BI 構成ページ](./media/PowerBIpage-before-edit.JPG)

2. **編集**を選択します。
3. **有効** オプションを **はい** に設定します。

    **Azure AD テナント** フィールドには、テナント (またはドメイン名) が表示されます。 たとえば、ContosoAX7.onmicrosoft.com テナントの Finance and Operations をプロビジョニングした場合、フィールドは前の図で示す値を持つ必要があります。 このフィールドが空白の場合は、適切なテナントを入力できます。

    Power BI 統合機能は実稼働前は機能せず、Azure AD ドメインをテストしないことに注意してください。 管理者ユーザー ツールを実行して、生産 Azure ADドメインを変更する必要があります。

4. **クライアント ID** フィールドで、前の手順で Power BI から取得した**クライアント ID** の値を入力します。
5. **アプリケーション キー** フィールドで、前の手順で Power BI から取得した**クライアント シークレット**の値を入力します。
6. **リダイレクト URL** フィールドが前の手順で Power BI に入力したものと同じリダイレクト URL に設定されていることを確認します。

    たとえば、Finance and Operations クライアントのベース URL をコピーして貼り付けてから OAuth の添え字を追加します。 次に例を示します: `http://contosoax7.cloud.dynamics.com/oauth`

7. **タイル フィルター テーブル** フィールドに、**会社** と入力します。 **タイル フィルター列**フィールドに、**ID** と入力します。

    これらの 2 つの値は、ワークスペースに固定された Power BI タイルのフィルタリングを有効にします。 例については、ワークスペースの会社コンテキストが **USMF** である場合、Power BI タイルのデータは USMF 会社に対してフィルター処理されます。

    Power BI のコンテンツに **会社** という名前のテーブルおよび **ID** という名前の列がある場合にのみ、会社のフィルターを適用することができます。 Finance and Operations によってリリースされた既存の Power BI コンテンツは、この会話を使用します。

    Power BI コンテンツに**会社**および **ID** という名前のテーブルとフィールドがそれぞれある場合、フィルターが無視され、タイルにフィルター処理されないデータが表示されます。

    ![タイル フィルター テーブルとタイル フィルターの列フィールド](media/1820cc9320b91814dbb7d7c90c04d49f.png)

8. **保存** を選択してページを閉じます。

## <a name="pin-tiles-to-a-workspace"></a>ワークスペースにタイルを固定

1. 設定を有効にするには、**元帳予算と予測** や **引当管理** などのワークスペースを開きます。 この例では、**元帳予算および予測**ワークスペースを使用します。

    **Power BI** セクションとバナーが表示されます。 右にスクロールすることが必要な可能性があります。

    ![Power BI セクションおよび元帳予算および予測ワークスペースのバナー](./media/Workspace.JPG)

3. バナーで、**使用開始**を選択します。 Finance and Operations の Power BI をはじめて使用する場合は、Finance and Operations クライアントから Power BI へのサインインを承認するように求められます。 **ここをクリックして Power BI に承認を与える** を選択します。

    ユーザーは、初めて Power BI コンテンツをピン留めするとき、このステップを完了する必要があります。

    ![Power BI の承認](./media/Authorize.JPG)

    > [!Note]
    > この手順に問題がある場合、**トラブルシューティングにおける一般的なエラー**セクションを参照し、**ユーザーが代わって会社データにアクセスするアプリケーションに同意できる**オプションに関する情報に留意します。

4. Azure AD の同意ページは、お客様の同意を求めます。 Finance and Operations がユーザーに代わって PowerBI.com にアクセスするには、ユーザーの同意が必要です。 **受け入れる** を選択します。

    ![同意ページ](media/65da7a9b5ac0a328568f76c4e7a0770c.png)

5. Finance and Operations の Azure AD に既にサインインしているので、再度資格情報を入力する必要はありません。 新しいタブが表示され、Finance and Operations と Power BI の間の接続を承認するように求められます。 接続を承認し元のタブに戻ります。
6. PowerBI.com アカウントのタイルの一覧が表示されます。 1 つまたは複数のタイルを選択し、選択したワークスペースにピン留めします。

## <a name="troubleshooting-common-errors"></a>一般的なエラーのトラブルシューティング

前の手順で**承諾**を選択した後、プロセスが失敗した場合、次のエラー メッセージが表示される場合があります。 エラーの詳細がメッセージの下部に表示されていることに注意します。 追加の技術情報は、原因を特定するのに役立つヒントを提供します (値は次の図で半透明)。

![エラー メッセージ](media/ce094da8b9e0674c5cbd75616e40d829.png)

### <a name="some-common-issues-and-the-resolution-steps"></a>一般的な問題および解決手順

| エラー                                                       | 解像度 |
|-------------------------------------------------------------|------------|
| 大文字と小文字の区別があるため、返信アドレスが一致しませんでした。 | Power BI に入力した URL は、アプリケーション ID と一致しない可能性があります。 Power BI を起動し、登録プロセスを再実行します。 |
| Power BI サービスは利用できません。                        | この問題は頻繁には発生しませんが、Power BI サービスに到達できないことがあります。 再登録する必要はありません。 後でタイルをワークスペースに固定してみてください。 |
| アプリケーションにアクセスすることはできません。                           | 登録プロセス中に、**手順 3 アクセスする API** の下のすべてのチェック ボックスが選択されなかった可能性があります。 Power BI を起動し、登録プロセスを再実行します。 |
| Power BI タイル ページは空です (コンテンツは表示されません)。     | PowerBI.com アカウントに、ダッシュ ボードまたはタイルがない可能性があります。 サンプル ダッシュ ボードなどのダッシュボードを追加して、もう一度をタイルをピン留めしてみてください。 |
| Power BI を許可する際のエラー                             | Azure 管理者ダッシュボード内の、**ユーザーおよびグループ > ユーザー設定** の下で、**ユーザーはアプリが会社のデータにアクセスすることに同意できる** オプションが **はい** に設定されていることを確認します。 |

## <a name="technical-details-about-oauth-20-authorization-code-grant-flow"></a>OAuth 2.0 承認コード付与フローに関する技術詳細

このセクションでは、認証フェーズ中にタイルのリストがユーザーに表示される直前に、Finance and Operations 間の許可フローと PowerBI.com サービスについて説明します。 Azure AD サービスでは、このフローを実行して、2 つのサービスがユーザーの代わりに安全に通信できるようにします。

次の図は、認証フローを示しています。

![認証フロー](media/caaddad46d4ea9e3c7e12e896733594a.png)

1. ユーザーが Finance and Operations 内のワークスペースに初めてアクセスすると、初回の接続の開始をユーザーに求めるメッセージが Power BI バナーに表示されます。 ユーザーが初めて接続を開始することに合意した場合、OAuth 2.0 承認コード付与フローが開始されます。
2. Finance and Operations はユーザー エージェントを Azure AD 承認エンドポイントにリダイレクトします。 同意が必要な場合、ユーザーは認証され、同意します。 ユーザーは Finance and Operations を実行しているため、既に Azure AD にサインインしています。 したがって、ユーザーは自分の資格情報を再度入力する必要はありません。
3. Azure AD 承認エンドポイントは、Azure AD エージェントを、認証コードと共にクライアント アプリケーションにもう一度リダイレクトします。 ユーザー エージェントは、クライアント アプリケーションのリダイレクト URL に認証コードを返します。 アプリケーション リダイレクト URL は、このトピックで説明するように、Power BI コンフィギュレーションで管理されるパラメーターです。
4. Finance and Operations にユーザーの代わりに認証コードが含まれているので、Azure AD トークン発行エンドポイントからアクセス トークンを要求します。 Finance and Operations は、ユーザーが同意したことを証明するための認証コードを表示します。
5. Azure AD トークン発行エンドポイントは、アクセス トークンと更新トークンを返します。 Finance and Operations は、Power BI からの視覚化を要求するアクセス トークンを持っている必要があります。 アクセス トークンは、短期間で有効期限が切れます。 更新トークンを使用して、新しいトークンを要求できます。
6. Finance and Operations はアクセス トークンを使用して、Power BI によって提供される Web API への認証をします。 Finance and Operations は、Web API を使用して、Power BI ビジュアル化がユーザーの代理として表示されるよう要求します。
7. クライアント アプリケーションが認証された後、Power BI Web API は、ユーザーに要求された視覚化を返します。 Power BI はユーザーが表示を許可されているデータのみを返すことに注意してください。 Power BI Web API はユーザーが Finance and Operations を介して接続していることを検出するため、ユーザーを正しく解決することができます。
8. ユーザーは、Finance and Operations ワークスペースで Power BI タイルを表示します。

その後のアクセスについては、このフロー全体は発生しません。 Finance and Operations はユーザーの代理としてアクセス トークンを持つため、手順 1. ～ 4. を繰り返す必要はありません。

## <a name="whats-next"></a>次の新機能

PowerBI.com 統合機能を有効にしたので、次の手順を実行します。

- 組織が PowerBI.com を使用している場合、ユーザーを招待して、彼ら自身の PowerBI.com アカウントのタイルおよびレポートをワークスペースにピン留めすると簡単にアクセスできます。
- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7月) またはそれ以降のバージョンを使用している場合、既成の分析ワークスペースが自分のワークスペースに組み込まれることがあります。 現在、この機能はマルチボックス環境でのみ使用できます。 以前のバージョンを使用している場合は、PowerBI.com アカウントに既製のレポートを配置することができます。 レポートは、Microsoft Dynamics Lifecycle Services (LCS) に配置されます。 
- エンティティ ストアで入出できるデータを使用して、独自の Power BI コンテンツを作成する場合があります。 (エンティティ格納とは、Finance and Operations に含まれる運用データウェアハウスのことです。) 詳細については、[エンティティ ストアとの Power BI の統合](power-bi-integration-entity-store.md) を参照してください。
- Finance and Operations に付属している既製の Power BI コンテンツと外部データをマッシュアップする可能性があります。 Power BI ソリューション テンプレートを使用して、このデータのマッシュアップを実行することができます。


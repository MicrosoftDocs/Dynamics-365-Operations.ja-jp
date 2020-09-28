---
title: Teams での休暇要求の管理
description: このトピックでは、Microsoft Teams で Dynamics 365 Human Resources アプリを使用して休暇を申請する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766763"
---
# <a name="manage-leave-requests-in-teams"></a>Teams での休暇要求の管理

[!include [banner](includes/preview-feature.md)]

Microsoft Teams の Microsoft Dynamics 365 Human Resources アプリを使用することで、簡単に休暇を申請することができ、Microsoft Teams で休暇の残日数情報を表示することができます。 ユーザーはボットと対話して情報を要求できます。 **休暇** タブには、より詳細な情報が表示されます。

## <a name="install-the-app"></a>アプリのインストール

Human Resources アプリは、Teams ストアにあります。

1. Microsoft Teams で省略記号を選択します。

   ![Teams Human Resources の休暇アプリの省略記号](./media/hr-teams-leave-app-ellipses.png)
 
2. Dynamics 365 Human Resources を検索し、**Human Resources**タイルを選択します。

   ![Teams Human Resources の休暇アプリの HR タイル](./media/hr-teams-leave-app-human-resources-tile.png)

3. **追加** ボタンを選択してアプリをインストールします。

   ![Teams Human Resources の休暇アプリのインストール](./media/hr-teams-leave-app-in-store.png)

アプリで自動的にサインインされなかった場合は、**設定** タブを選択してサイン インします。

![Teams Human Resources 休暇アプリの設定タブ](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> [サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。 

複数の Human Resources インスタンスへのアクセス許可がある場合は、 **設定** タブで接続先の環境を選択でき ます。

> [!WARNING]
> 現在、このアプリはシステム管理者のセキュリティ ロールに対応していません。システム管理者アカウントでログインすると、エラーメッセージが表示されます。 別のアカウントでログインするには、**設定** タブで **アカウントの切り替え** ボタンを選択し、システム管理者権限のないユーザー アカウントでログインします。
 
## <a name="use-the-bot"></a>ボットの使用

アプリをインストールすると、ボットが代理で実行できるアクションの種類を通知するウェルカム メッセージが表示されます。

![Human Resources Teams 休暇アプリがウェルカム メッセージを表示します](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> 初めてボットと通信する際には、サイン インする必要があります。 [サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。

ボットには次の依頼ができます:

- 登録されている休暇タイプごとに、休暇残数情報を表示する。

   ![Teams Human Resources 休暇アプリが残日数を表示します](./media/hr-teams-leave-app-bot-balances.png)
 
- 特定の休暇タイプに関する追加情報を表示する。

   ![Teams Human Resources 休暇アプリが詳細情報を表示します](./media/hr-teams-leave-app-bot-details.png)

- 休暇申請を開始する。

   ![Teams Human Resources 休暇アプリが休暇を申請します](./media/hr-teams-leave-app-bot-request.png)
 
休暇申請を開始した後、カード内で日数を調整できます。

![Teams Human Resources 休暇アプリが申請を編集します](./media/hr-teams-leave-app-bot-edit.png)
 
情報の入力が完了したら、**送信** を選択して、承認のために送信します。 また、**下書きとして保存**を選択すると、後で処理の続きを進めることができます。

![Teams Human Resources 休暇アプリが申請を送信します](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Teams で休暇を管理する

**休暇** タブでは、次の情報を表示できます:

- 登録されている休暇タイプごとに、休暇残数の情報を表示する

- 今後の休暇依頼

- 休暇申請

- 休暇申請の下書き

![Teams Human Resources 休暇アプリの休暇タブ](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>新しい製品の作成

1. **新規作成** を選択して、新しい休暇申請を作成する。

   ![Teams Human Resources 休暇アプリの新規申請](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. 休暇の日付または日数を入力し、**追加** を選択します。

   ![Teams Human Resources 休暇アプリが休暇を追加します](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. 必要に応じて、理由コードを入力します。 また、コメントを入力して添付ファイルを追加します。

4. 情報の入力が完了後は、**提出**と入力して承認を依頼します。 また、**下書きとして保存**と入力すると、後で処理の続きを進めることができます。

### <a name="manage-draft-requests"></a>申請の下書きを管理する

1. **下書き**タブを選択します。

   ![Teams Human Resources 休暇アプリの下書きタブ](./media/hr-teams-leave-app-drafts-tab.png)

2. 申請を編集するには鉛筆アイコンを選択するか、[ごみ箱] を選択することで申請を削除できます。

3. 必要な変更を行います。 情報の入力が完了後は、**提出**と入力して承認を依頼します。 また、**下書きとして保存**を選択すると、後で処理の続きを進めることができます。

   ![Teams Human Resources 休暇アプリが下書きを編集します](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a>Teams の通知

自分または自分が承認者である作業者が休暇申請を送信すると、Teams の Human Resources アプリで通知を受け取ります。 通知を選択して表示することができます。 通知は、**チャット** 領域にも表示されます。

承認者の場合は、通知で **承認** または **拒否** を選択できます。 オプション メッセージを指定することもできます。

![Teams の Human Resources アプリの休暇申請通知](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a>チームの休暇カレンダーの表示

直属の部下を持つマネージャーの場合は、チームの承認済みおよび保留中の休暇を表示できます。

1. Teams の Human Resources アプリで、**休暇** を選択します。

2. **チーム カレンダー** を選択します。

   ![Teams の Human Resources アプリでカレンダーを表示](./media/hr-teams-leave-app-view-calendar.png)

カレンダーには、直属の部下の承認済と保留中の休暇が表示されます。

![Teams の Human Resources アプリの休暇カレンダー](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a>プライバシー通知

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding インテリジェント サービス (LUIS)

Microsoft Teams で Dynamics 365 Human Resources Botを使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。 ユーザーが入力した 「顧客 Contoso を検索」は、言語理解インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。 LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。 LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。 この情報は、Microsoft の  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) に渡され、 Dynamics 365 Human Resources からのデータと対話し、ユーザー クエリに目的の情報を取得します。 

ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。 LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。 LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure ボット フレームワークに送信される可能性があります。 

ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。 認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。 

Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>Microsoft Azure Event Grid と Microsoft Teams

Teams 内で Dynamics 365 Human Resources アプリの通知機能を使用する場合、特定の顧客データは、テナントの Human Resources サービスが展開される地域外に流出します。 Dynamics 365 Human Resources は、従業員の休暇申請とワークフロー タスクの詳細を Microsoft Azure Event Grid と Microsoft Teams に送信します。 このデータは、最大 24 時間保存され、米国で処理され、転送中および保存中に暗号化され、トレーニングやサービスの改善のために Microsoft またはそのサブプロセッサによって使用されることはありません。

## <a name="see-also"></a>参照

[Microsoft Teams のダウンロードとインストール](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams ヘルプ センター](https://support.office.com/teams)</br>
[Teams の Human Resources アプリ](hr-admin-teams-leave-app.md)

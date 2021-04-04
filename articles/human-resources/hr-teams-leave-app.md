---
title: Teams での休暇要求の管理
description: このトピックでは、Microsoft Teams で Dynamics 365 Human Resources アプリを使用して休暇を申請する方法について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/23/2021
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
ms.openlocfilehash: 79bded5a241a8d5de1847adff3e663359ce1b26f
ms.sourcegitcommit: d7c18228256daeefbf6518c3ef82fed4f7dbc161
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571731"
---
# <a name="manage-leave-requests-in-teams"></a>Teams での休暇要求の管理

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Teams の Dynamics 365 Human Resources アプリを使用することで、簡単に休暇を申請することができ、Microsoft Teams で休暇の残日数情報を表示することができます。 ボットと対話して情報を要求し、休暇申請を開始することができます。 **休暇** タブには、より詳細な情報が表示されます。 さらに、Human Resources アプリ外部の Teams やチャットで今後の休暇についての情報を送信することもできます。

## <a name="install-the-app"></a>アプリのインストール

Dynamics 365 Human Resources アプリは、Teams ストアにあります。

1. Microsoft Teams で省略記号を選択します。

   ![Teams Human Resources の休暇アプリの省略記号](./media/hr-teams-leave-app-ellipses.png)
 
2. Dynamics 365 Human Resources を検索し、**Human Resources** タイルを選択します。

   ![Teams Human Resources の休暇アプリの HR タイル](./media/hr-teams-leave-app-human-resources-tile.png)

3. **追加** ボタンを選択してアプリをインストールします。

   ![Teams Human Resources の休暇アプリのインストール](./media/hr-teams-leave-app-in-store.png)

アプリで自動的にサインインされなかった場合は、**設定** タブを選択してサイン インします。

![Teams Human Resources 休暇アプリの設定タブ](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> [サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。 

複数の Human Resources インスタンスへのアクセス許可がある場合は、 **設定** タブで接続先の環境を選択でき ます。

> [!NOTE]
> アプリはシステム管理者セキュリティ ロールをサポートするようになりました。
 
## <a name="use-the-bot"></a>ボットの使用

アプリをインストールすると、ボットが代理で実行できるアクションの種類を通知するウェルカム メッセージが表示されます。

![Human Resources Teams 休暇アプリがウェルカム メッセージを表示します](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> 初めてボットと通信する際には、サイン インする必要があります。 [サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定でポップアップを許可しているかどうかを確認してください。

ボットには次の依頼ができます:

- 休暇申請を開始する。

  ![Teams チャットでの休暇申請の開始](./media/hr-teams-leave-app-initiate.png)

- チャット ボットでユーザーの休暇申請を入力します。 **休暇申請** を選択し、申請の詳細を編集します。

  ![休暇申請詳細情報の編集](./media/hr-teams-leave-app-details.png)

- 休暇申請詳細情報の編集が完了したら、**送信** を選択して、承認を依頼します。

  ![休暇申請の送信](./media/hr-teams-leave-app-submit.png)

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

4. 情報の入力が完了後は、**提出** と入力して承認を依頼します。 また、**下書きとして保存** と入力すると、後で処理の続きを進めることができます。

### <a name="manage-draft-requests"></a>申請の下書きを管理する

1. **下書き** タブを選択します。

   ![Teams Human Resources 休暇アプリの下書きタブ](./media/hr-teams-leave-app-drafts-tab.png)

2. 申請を編集するには鉛筆アイコンを選択するか、[ごみ箱] を選択することで申請を削除できます。

3. 必要な変更を行います。 情報の入力が完了後は、**提出** と入力して承認を依頼します。 また、**下書きとして保存** を選択すると、後で処理の続きを進めることができます。

   ![Teams Human Resources 休暇アプリが下書きを編集します](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a>Teams 通知への対応

自分または自分が承認者である作業者が休暇申請を送信すると、Teams の Human Resources アプリで通知を受け取ります。 通知を選択して表示することができます。 通知は、**チャット** 領域にも表示されます。

承認者の場合は、通知で **承認** または **拒否** を選択できます。 オプション メッセージを指定することもできます。

![Teams の Human Resources アプリの休暇申請通知](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>同僚に次の休暇情報を送信する

Teams 向けの Human Resources アプリをインストールすると、チームやチャットで今後の休暇の情報を同僚に簡単に送信できます。

1. チームまたは Teams のチャットで、チャット ウィンドウの下にある人事管理ボタンを選択します。

   ![チャット ウィンドウの下の人事管理ボタン](./media/hr-teams-leave-app-chat-button.png)

2. 共有する休暇申請を選択します。 休暇申請の下書きを共有する場合は、まず **下書き** を選択します。

   ![共有する今後の休暇申請の選択](./media/hr-teams-leave-app-chat-search.png)

休暇申請がチャットに表示されます。

![Human Resources の休暇申請カード](./media/hr-teams-leave-app-chat-card.png)

申請の下書きを共有すると、下書きとして表示されます。

![Human Resources の休暇申請カードの下書き](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a>チームの休暇カレンダーの表示

直属の部下を持つマネージャーの場合は、チームの承認済みおよび保留中の休暇を表示できます。

1. Teams の Human Resources アプリで、**休暇** を選択します。

2. **チーム カレンダー** を選択します。 カレンダーには、直属の部下の承認済と保留中の休暇が表示されます。

   ![Teams の Human Resources アプリでカレンダーを表示](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > チーム カレンダーが表示できない場合は、有効にできるよう管理者に問い合わせてください。 詳細については、[インストールと設定](hr-admin-teams-leave-app.md#install-and-setup)を参照してください。

## <a name="supported-languages"></a>対応している言語

Teams の Dynamics 365 Human Resources アプリでは、次の言語がサポートされます。

| ロケール ID | 言語 |
| --- | --- |
| de-DE | ドイツ語 (ドイツ) |
| es-ES | スペイン語 (スペイン) |
| es-MX | スペイン語 (メキシコ) |
| fr-CA | フランス語 (カナダ) |
| fr-FR | フランス語 (フランス) |
| it-IT | イタリア語 (イタリア) |
| nl-NL | オランダ語 (オランダ) |
| pt-BR | ポルトガル語 (ブラジル) |
| tr-TR | トルコ語 (トルコ) |
| zh-CN | 中国語 (簡体) |

## <a name="troubleshooting"></a>トラブルシューティング

Dynamics 365 Human Resources Teams アプリへのサインインまたは使用で問題が発生した場合は、次のトラブルシューティングの手順を実行してください。 トラブルシューティング後も問題が解決しない場合は、サポートにお問い合わせください。 詳細については、[サポート](hr-admin-troubleshooting-support.md) を参照してください。

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Teams の Human Resources アプリにサインインできない

アプリにサインインできない場合は、Microsoft Teams へのサインインに使用しているアカウントが Dynamics 365 Human Resources の従業員レコードに関連付けられていない可能性があります。 システム管理者に連絡して、従業員レコードが正しく関連付けられていることを確認してください。

### <a name="translations-dont-display-correctly"></a>翻訳が正しく表示されない

翻訳が期待した通りに表示されない場合は、Teams で選択する言語が Human Resources **ユーザー オプション** で選択された言語と一致していることを確認してください。

Teams で、**設定** の **アプリ言語** を確認します。

![Teams の設定](./media/hr-teams-leave-app-settings.png)

Human Resources で、**設定** を選択してから、**ユーザー オプション** を選択します。 **言語** フィールドが Teams の **アプリ言語** フィールドと一致していることを確認します。

![Human Resources ユーザー オプション](./media/hr-teams-leave-app-user-options.png)

それでも翻訳の問題が発生する場合は、お知らせください。 詳細については、[Finance and Operations アプリまたは Lifecycle Services (LCS) のサポートを得る](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-support?toc=/dynamics365/human-resources/toc.json)を参照してください。

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Teams の Human Resources アプリで休暇申請を承認する際のエラー

Teams アプリで休暇申請を承認しようとしたときにエラーが発生した場合は、次のトラブルシューティングの手順を実行します。

1. Microsoft Teams へのサインインに使用しているアカウントが、Dynamics 365 Human Resources にアクセスに使用しているアカウントと同じであることを確認します。

2. 休暇承認のワークフロー設定を確認して、要求の有効な承認者であることを確認します。 休暇申請ワークフローの詳細については、[休暇申請ワークフローの作成](hr-leave-and-absence-workflow.md) を参照してください。

## <a name="known-accessibility-issues"></a>既知のアクセシビリティの問題

Teams の Human Resources アプリには、今後のリリースに向けて修正を行っている次のようなアクセシビリティ上の問題があります。

| 出庫 | 回避策または説明 |
| --- | --- |
| デスクトップで 400% に拡大すると、一部のアクション ボタンが表示されない場合があります。 | この拡大のレベルがサポートされるまで、代わりに拡大鏡を使用することをお勧めします。 |
| **休暇** タブで、VoiceOver が、タイムアウト グリッドのヘッダーを読みながら、ボタンのアクションを読み上げます。 | グリッド内のヘッダーと要素は年によってグループ化され、折りたたむことができます。 VoiceOver は、これをアクション可能な項目として解釈しますが、アクション可能ではありません。 |
| **休暇** タブで、新しい要求の **理由コード** へ移動する際に追加のスワイプ ジェスチャがあります。 | スワイプ ナビゲーションがアクセスしようとしている非表示のコントロールはありません。 |
| **休暇** タブで、カレンダーが開いている状態でスワイプすると、新しい要求の上部または要求の編集中に移動するのではなく、コントロールの外部に出てしまいます。 | **今日に移動** が表示された場合、コントロールの最後で逆方向にスワイプして一番上に戻ることを検討してください。 |
| **チャット** タブで、支援ツールまたはキーボードのナビゲーションを使用して日付を入力すると、フォーカスが上に戻ってきます。 | 入力領域に戻るまでタブを押し続けます。 |

## <a name="privacy-notice"></a>プライバシー通知

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding インテリジェント サービス (LUIS)

Microsoft Teams で Dynamics 365 Human Resources Botを使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。 ユーザーが入力した 「顧客 Contoso を検索」は、言語理解インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。 LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。 LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。 この情報は、Microsoft の  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) に渡され、 Dynamics 365 Human Resources からのデータと対話し、ユーザー クエリに目的の情報を取得します。 

ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。 LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。 LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure ボット フレームワークに送信される可能性があります。 

ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。 認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。 

Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams、Azure Event Grid、Azure Cosmos DB

Microsoft Teams 内で Dynamics 365 Human Resources アプリを使用する場合、特定の顧客データが、テナントの Human Resources サービスが展開されている地域外に流出する可能性があります。

Dynamics 365 Human Resources は、従業員の休暇申請とワークフロー タスクの詳細を Microsoft Azure Event Grid と Microsoft Teams に送信します。 このデータは、Microsoft Azure Event Grid に最大 24 時間保存でき、米国内で処理され、転送中および保存中に暗号化され、トレーニングやサービスの改善のために Microsoft またはそのサブプロセッサによって使用されることはありません。 データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) を参照してください。

Human Resources アプリでチャット ボットと会話しながら、会話の内容を Azure Cosmos DB に保存し、Microsoft Teams に送信することができます。 このデータは Azure Cosmos DB に最大24時間格納され、テナントの Human Resources サービスが展開されている地域外で処理される可能性があり、転送中および保存中に暗号化され、トレーニングやサービス改善のために Microsoft またはそのサブプロセッサが使用することはありません。 データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true) を参照してください。
 
組織または組織内のユーザーの Microsoft Teams の Human Resources アプリへのアクセスを制限するには、[Microsoft Teams におけるアプリのアクセス許可ポリシーの管理](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies) を参照してください。

## <a name="see-also"></a>参照

[Microsoft Teams のダウンロードとインストール](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams ヘルプ センター](https://support.office.com/teams)</br>
[Teams の Human Resources アプリ](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
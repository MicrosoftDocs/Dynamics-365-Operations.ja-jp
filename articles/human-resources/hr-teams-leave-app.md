---
title: Teams での休暇要求の管理
description: このトピックでは、Microsoft Teams で Dynamics 365 Human Resources アプリを使用して休暇を申請する方法について説明します。
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d004e33d01dbd171626d7e23f93df081bc0210a9
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924750"
---
# <a name="manage-leave-requests-in-teams"></a>Teams での休暇要求の管理

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Teams の Dynamics 365 Human Resources アプリを使用することで、簡単に休暇を申請することができ、Microsoft Teams で休暇の残日数情報を表示することができます。 ボットと対話して情報を要求し、休暇申請を開始することができます。 **休暇** タブには、より詳細な情報が表示されます。 さらに、Human Resources アプリ外部の Teams やチャットで今後の休暇についての情報を送信することもできます。

## <a name="install-the-app"></a>アプリのインストール

Dynamics 365 Human Resources アプリは、Teams ストアにあります。

1. Microsoft Teams で、アプリケーションの一覧に移動します。
 
2. Dynamics 365 Human Resources を検索し、**Human Resources** タイルを選択します。

> [!NOTE]
> 2021 年 12 月 20 日以降、Microsoft テナントにホストされている人事管理アプリのボット サービス (バージョン 1.1.4) は廃止されます。 最新の拡張機能 (バージョン1.1.5) をインストールできます。 詳細については、[Teams で休暇申請を管理する](hr-admin-teams-leave-app.md#update-app) を参照してください。

3. **追加** ボタンを選択してアプリをインストールします。

アプリで自動的にサインインされなかった場合は、**設定** タブを選択してサイン インします。

> [!NOTE]
> [サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定を更新してポップアップを許可してください。 

複数の Human Resources インスタンスへのアクセス許可がある場合は、 **設定** タブで接続先の環境を選択でき ます。

> [!NOTE]
> アプリはシステム管理者セキュリティ ロールをサポートするようになりました。
 
## <a name="use-the-bot"></a>ボットの使用

アプリをインストールすると、ボットが代理で実行できるアクションの種類を通知するウェルカム メッセージが表示されます。

> [!NOTE]
> 初めてボットと通信する際には、サイン インする必要があります。 [サインイン] ダイアログ ボックスが表示されない場合は、ブラウザーの設定を更新してポップアップを許可してください。

ボットには次の依頼ができます:

- 現在の休暇残数を表示します。 たとえば、「休暇残数を表示する」というメッセージが表示されます。

- 休暇申請を開始する。 たとえば、「休暇を取ってください」や「来週の木曜と金曜に休暇を取りたいのですが」というメッセージを送信すると、休暇の種類に応じた休暇申請がより具体的にできます。 

  ![Teams チャットでの休暇申請の開始。](./media/hr-teams-leave-app-initiate.png)

- チャット ボットでユーザーの休暇申請を入力します。 **休暇申請** を選択し、申請の詳細を編集します。

   同じ日に複数の休暇タイプの休暇申請を行いたい場合は、**その他オプション** メニューから **日の分割** オプションを選択します。 

   休暇申請の単位が日数の場合に半日休暇を選択した場合は、**その他のオプション** メニューから **半日の定義** を選択することで、最初の半日と後半の半日のどちらに休暇を申請するかを指定できます。
   
   ![半日の定義。](./media/HalfDayDefinitions.png)

- 休暇申請詳細情報の編集が完了したら、**送信** を選択して、承認を依頼します。

  ![休暇申請の送信。](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>Teams で休暇を管理する

**休暇** タブでは、次の情報を表示できます: 

- 登録されている休暇タイプごとに、休暇残数の情報を表示する

- 今後の休暇依頼

- 休暇申請

- 休暇申請の下書き
 
### <a name="create-a-new-request"></a>新しい製品の作成

1. **新規作成** を選択して、新しい休暇申請を作成する。

2. 休暇の日付または日数を入力し、**追加** を選択します。

   ![Teams Human Resources 休暇アプリが休暇を追加します。](./media/TimeOffHours.png)

3. 必要に応じて、理由コードを入力します。 また、コメントを入力して添付ファイルを追加します。

4. 異なる休暇タイプで同じ日に複数の休暇申請を行う場合は、**その他のオプション** メニューから **日の分割** を選択します。

5. **半日の定義** オプションを選択して、最初の半日の休みを要求するか、後半の半日の休みを要求するかを指定します。 このオプションは、休暇要求単位が日数で、要求量が 0.5 日の場合に使用できます。

6. 情報の入力が完了したら、**送信** を選択して、承認をリクエストします。 また、**下書きとして保存** と入力すると、後で処理の続きを進めることができます。

### <a name="manage-draft-requests"></a>申請の下書きを管理する

1. **下書き** タブを選択します。

2. 申請を編集するには鉛筆アイコンを選択するか、[ごみ箱] を選択することで申請を削除できます。

3. 必要な変更を行います。 情報の入力が完了後は、**提出** と入力して承認を依頼します。 また、**下書きとして保存** を選択すると、後で処理の続きを進めることができます。
   
### <a name="respond-to-teams-notifications"></a>Teams 通知への対応

自分または自分が承認者である作業者が休暇申請を送信すると、Teams の Human Resources アプリで通知を受け取ります。 通知を選択して休暇申請を表示することができます。 通知は、**チャット** 領域にも表示されます。

承認者の場合は、通知で **承認** または **拒否** を選択できます。 オプション メッセージを指定することもできます。

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>同僚に次の休暇情報を送信する

Teams 向けの Human Resources アプリをインストールすると、チームやチャットで今後の休暇の情報を同僚に簡単に送信できます。

1. チームまたは Teams のチャットで、チャット ウィンドウの下にある人事管理ボタンを選択します。

   ![チャット ウィンドウの下の人事管理ボタン。](./media/hr-teams-leave-app-chat-button.png)

2. 共有する休暇申請を選択します。 休暇申請の下書きを共有する場合は、まず **下書き** を選択します。

休暇申請がチャットに表示されます。

申請の下書きを共有すると、下書きとして表示されます。

## <a name="view-your-teams-leave-calendar"></a>チームの休暇カレンダーの表示

直属の部下を持つマネージャーの場合は、チームの承認済みおよび保留中の休暇を表示できます。

1. Teams の Human Resources アプリで、**休暇** を選択します。

2. **チーム カレンダー** を選択します。 カレンダーには、直属の部下の承認済と保留中の休暇が表示されます。

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

Dynamics 365 Human Resources Teams アプリへのサインインまたは使用で問題が発生した場合は、次のトラブルシューティングの手順を実行してください。 トラブルシューティング後も問題が解決しない場合は、サポートにお問い合わせください。 詳細については、[サポート](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照してください。

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Teams の Human Resources アプリにサインインできない

アプリにサインインできない場合は、Microsoft Teams へのサインインに使用しているアカウントが Dynamics 365 Human Resources の従業員レコードに関連付けられていない可能性があります。 システム管理者に連絡して、従業員レコードが正しく関連付けられていることを確認してください。

### <a name="cant-find-the-dynamics-365-human-resources-environment-in-settings"></a>設定で Dynamics 365 Human Resources 環境が見つらない

正しい Dynamics 365 環境を選択できない場合、ユーザー レコードが正しく同期されていない可能性があります。 システム管理者に問い合わせて、ユーザー レコードを再作成し、そのユーザー資格情報を関連付けしてください。 次に、数分後に Microsoft Teams の Human Resources アプリケーションにログインしてください。

### <a name="translations-dont-display-correctly"></a>翻訳が正しく表示されない

翻訳が期待した通りに表示されない場合は、Teams で選択する言語が Human Resources **ユーザー オプション** で選択された言語と一致していることを確認してください。

Teams で、**設定** の **アプリ言語** を確認します。

![Teams の設定。](./media/hr-teams-leave-app-settings.png)

Human Resources で、**設定** を選択してから、**ユーザー オプション** を選択します。 **言語** フィールドが Teams の **アプリ言語** フィールドと一致していることを確認します。

![Human Resources ユーザー オプション。](./media/hr-teams-leave-app-user-options.png)

それでも翻訳の問題が発生する場合は、お知らせください。 詳細については、[Finance and Operations アプリまたは Lifecycle Services (LCS) のサポートを得る](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)を参照してください。

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Teams の Human Resources アプリで休暇申請を承認する際のエラー

Teams アプリで休暇申請を承認しようとしたときにエラーが発生した場合は、次のトラブルシューティングの手順を実行します。

1. Microsoft Teams へのサインインに使用しているアカウントが、Dynamics 365 Human Resources にアクセスに使用しているアカウントと同じであることを確認します。

2. 休暇承認のワークフロー設定を確認して、要求の有効な承認者であることを確認します。 休暇申請ワークフローの詳細については、[休暇申請ワークフローの作成](hr-leave-and-absence-workflow.md) を参照してください。

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>休暇承認者が休暇申請を承認するための Teams のチャット メッセージを受信しない

1. 通知が環境およびユーザーに対して有効になっている必要があります。 詳細については、[Teams の Human Resources アプリで通知を有効にする](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) および[個々のユーザーの Teams の通知をオンまたはオフにする](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) を参照してください。

2. ユーザーが休暇申請を承認するために使用するのと同じ資格情報で **チャット** タブにログインしていることを確認します。 "サインアウト" というメッセージを使用してから "サインイン" を使用して正しい資格情報でサインインします。

3. それでも問題が解消しない場合は、システム管理者として **ビジネス イベント システム** バッチ ジョブのステータスを確認します。 **待機中** または **実行中** のステージにある場合は、数分後にもう一度戻って確認します。 ステータスが変わらない場合は、弊社のチームで問題を解決することができるように、サポート チケットを記録します。

## <a name="known-accessibility-issues"></a>既知のアクセシビリティの問題

Teams の Human Resources アプリには、今後のリリースに向けて修正を行っている次のようなアクセシビリティ上の問題があります。

| 出庫 | 回避策または説明 |
| --- | --- |
| デスクトップで 400% に拡大すると、一部のアクション ボタンが表示されない場合があります。 | この拡大のレベルがサポートされるまで、代わりに拡大鏡を使用することをお勧めします。 |
| **休暇** タブで、VoiceOver が、タイムアウト グリッドのヘッダーを読みながら、ボタンのアクションを読み上げます。 | グリッド内のヘッダーと要素は年によってグループ化され、折りたたむことができます。 VoiceOver は、この表示をアクション可能な項目として解釈しますが、アクション可能ではありません。 |
| **休暇** タブで、新しい要求の **理由コード** へ移動する際に追加のスワイプ ジェスチャがあります。 | スワイプ ナビゲーションがアクセスしようとしている非表示のコントロールはありません。 |
| **休暇** タブで、カレンダーが開いている状態でスワイプすると、新しい要求の上部または要求の編集中に移動するのではなく、コントロールの外部に出てしまいます。 | **今日に移動** が表示された場合、コントロールの最後で逆方向にスワイプして一番上に戻ることを検討してください。 |
| **チャット** タブで、支援ツールまたはキーボードのナビゲーションを使用して日付を入力すると、フォーカスが上に戻ってきます。 | 入力領域に戻るまでタブを押し続けます。 |

## <a name="privacy-notice"></a>プライバシー通知

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding インテリジェント サービス (LUIS)

Microsoft Teams で Dynamics 365 Human Resources Bot を使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。 ユーザーが入力した「顧客 Contoso を検索」は、言語理解インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。 LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。 LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。 この情報は、Microsoft の [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) に渡され、 Dynamics 365 Human Resources からのデータと対話し、ユーザー クエリに目的の情報を取得します。 

ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。 LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。 LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure Bot Framework に送信される可能性があります。 

ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。 認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。 

Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams、Azure Event Grid、Azure Cosmos DB

Microsoft Teams 内で Dynamics 365 Human Resources アプリを使用する場合、特定の顧客データが、テナントの Human Resources サービスが展開されている地域外に流出する可能性があります。

Dynamics 365 Human Resources は、従業員の休暇申請とワークフロー タスクの詳細を Microsoft Azure Event Grid と Microsoft Teams に送信します。 このデータは、Microsoft Azure Event Grid に最大 24 時間保存でき、米国内で処理され、転送中および保存中に暗号化され、トレーニングやサービスの改善のために Microsoft またはそのサブプロセッサによって使用されることはありません。 データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide) を参照してください。

Human Resources アプリでチャット ボットと会話しながら、会話の内容を Azure Cosmos DB に保存し、Microsoft Teams に送信することができます。 このデータは Azure Cosmos DB に最大24時間格納され、テナントの Human Resources サービスが展開されている地域外で処理される可能性があり、転送中および保存中に暗号化され、トレーニングやサービス改善のために Microsoft またはそのサブプロセッサが使用することはありません。 データが Teams 内のどこに格納されているかを把握するには、[Microsoft Teams 内のデータの場所](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide) を参照してください。
 
組織または組織内のユーザーの Microsoft Teams の Human Resources アプリへのアクセスを制限するには、[Microsoft Teams におけるアプリのアクセス許可ポリシーの管理](/MicrosoftTeams/teams-app-permission-policies) を参照してください。

## <a name="see-also"></a>参照

[Microsoft Teams のダウンロードとインストール](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams ヘルプ センター](https://support.office.com/teams)</br>
[Teams の Human Resources アプリ](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

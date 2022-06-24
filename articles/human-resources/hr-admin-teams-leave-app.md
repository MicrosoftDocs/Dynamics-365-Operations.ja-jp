---
title: Teams の Human Resources アプリ
description: この記事では、Microsoft Teams における Microsoft Dynamics 365 Human Resources について説明します。
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a7ff576efbfeb0c5383a48756fdd7e79f1abdba2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902259"
---
# <a name="human-resources-app-in-teams"></a>Teams の Human Resources アプリ


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Teams の Microsoft Dynamics 365 Human Resources アプリを使用すると、従業員は簡単に休暇を申請することができ、Microsoft Teams にて休暇の残日数情報を表示することができます。 従業員は bot と対話して情報を要求できます。 **休暇** タブには、より詳細な情報が表示されます。 さらに、Human Resources アプリの外部で、チームやチャットで今後の休暇に関する情報を送信できます。

![Teams Human Resources の休暇アプリ ボット。](./media/hr-teams-leave-app-bot.png)

![Teams Human Resources 休暇アプリの休暇タブ。](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources の休暇申請カード。](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>インストールと設定

Dynamics 365 Human Resources アプリは、Teams ストアにあります。 Teams アプリのインストールについては、[Teams で休暇申請を管理する](hr-teams-leave-app.md)を参照してください 。

Teams におけるアプリのアクセス許可の管理については、[Microsoft Teams におけるアプリのアクセス許可ポリシーを管理する](/MicrosoftTeams/teams-app-permission-policies)を参照してください。

ユーザーがアプリで休暇および欠勤カレンダーを表示するには、機能管理で **Teams の休暇および欠勤カレンダー** を有効にする必要があります。 機能を有効にする方法については、[機能の管理](hr-admin-manage-features.md)を参照してください。

## <a name="update-app"></a>アプリの更新
>[!NOTE]
> 2021 年 12 月 20 日以降、Microsoft テナントにホストされている人事管理アプリのボット サービスは廃止されます。 最新の拡張機能 (バージョン1.1.5) がインストール可能なため、影響はありません。 主な影響は、古いの拡張機能 (バージョン1.1.4) で発生します。 当該バージョンのチャット ボットは動作しなくなります。 **休暇** タブは引き続き両方の拡張機能で使用できます。

バージョン 1.1.4 では、チャットボットがメッセージに一切応答しなくなります。 たとえば、**サインイン**、**残高を表示する**、**休暇を表示する** などです。 アプリを手動で最新版に更新する必要があります。 詳細については、[Microsoft Teams のアプリを更新する](/MicrosoftTeams/apps-update-experience) を参照してください。

バージョン 1.1.5 に更新するには、次の手順を実行します:
1. Microsoft Teams で、**アプリ** に移動します。
2. **人事管理** アプリを探します。
3. **アップグレード** を選択します。

人事管理アプリのバージョンは、**バージョン情報** タブまたは **個人用アプリ** セクションで確認できます。 

![人事管理の **バージョン情報** タブ。](./media/HR-teams-about.png)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Teams の Human Resources アプリの通知を有効にする

ユーザーが Teams アプリで休暇申請通知を受け取るようにするには、Dynamics 365 Human Resources で通知を有効にする必要があります。

>[!NOTE]
>Teams にサインインしていて、Teams の Dynamics 365 Human Resources アプリを使用しているユーザーだけが、通知を受け取ります。

1. 人事管理では、**システム管理** を選択します。

2. **リンク** を選択します。

3. **設定** で **システム パラメータ** を選択します。

4. **一般** タブで **Teams アプリの通知を有効にする** を **はい** に設定します。

   ![システム パラメータで Teams アプリの通知を有効にする。](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. すべてのユーザーに対して Teams の通知をオンにするには、プロンプトで **はい** を選択します。

   ![すべてのユーザーに対して Teams の通知を有効にする。](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>個々のユーザーの Teams の通知をオンまたはオフにする

Teams の Dynamics 365 Human Resources アプリの通知を有効にした後、ユーザーごとに通知をオンまたはオフにすることができます。

1. 人事管理では、**システム管理** を選択します。

2. **リンク** を選択します。

3. **ユーザー** で **ユーザー オプション** を選択します。

4. **ワークフロー** タブを選択します。

5. **Teams アプリの通知を有効にする** を **はい** に設定するとユーザーへの通知が有効になり、**いいえ** に設定するとユーザーへの通知が無効になります。

   ![ユーザー オプションのワークフロー タブで Teams アプリの通知を有効にする。](./media/hr-admin-teams-leave-app-notifications.png)

6. **保存** を選択します。

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

## <a name="notes"></a>摘要

今後のリリースでは、次の作業項目が予定されています。

| 作業項目 | 状態 |
| --- | --- |
| 未来日付の休暇を送信する場合に、残日数に誤りがあることを示します。 | 予測機能は未実装です。 現在日付の残日数が表示されます。 |
| **レビュー中** の申請をキャンセルできない 。 | この機能には現在対応していないため、今後のリリースで対応予定です。 |
| 残日数情報が、現日付の時点に基づいて算出される。 | システムでは現在、**休暇と欠勤のパラメータ** ページで構成されている場合であっても、見越計上期間の残日数は表示されません。 |

## <a name="troubleshooting"></a>トラブルシューティング

ユーザーが Teams の Human Resources アプリへのサインインまたは使用で問題が発生した場合は、次のトラブルシューティングの手順を実行してください。 トラブルシューティング後も問題が解決しない場合は、サポートにお問い合わせください。 詳細については、[サポート](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照してください。

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Teams Human Resources アプリケーションを最新の情報に更新する
Teams Human Resources アプリで問題が発生した場合、最新バージョンを使用しているかどうかを確認する必要があります。 サポートされる最小バージョンは、1.1.5 です。 Teams アプリケーションを更新する手順については、[Teams のドキュメント](/MicrosoftTeams/apps-update-experience)を 参照してください。

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Teams の Human Resources アプリにサインインできない

ユーザーがアプリにサインインできないために連絡した場合は、そのユーザーが Human Resources に関連付けられている従業員レコードを持っていることを確認します。

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Teams の Human Resources アプリで休暇申請を承認する際のエラー

Teams アプリで休暇申請を承認しようとしたときにユーザーがエラーを受信した場合は、次のトラブルシューティングの手順を試行します。

1. Teams のアカウントが、Human Resources へのアクセスに使用するものと同じであることを確認します。

2. 休暇承認のワークフロー設定を確認して、要求の有効な承認者であることを確認します。 休暇申請ワークフローの詳細については、[休暇申請ワークフローの作成](hr-leave-and-absence-workflow.md) を参照してください。

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>休暇承認者が休暇申請を承認するための Teams のチャット メッセージを受信しない

1. 通知が環境およびユーザーに対して有効になっている必要があります。 詳細については、[Teams の Human Resources アプリで通知を有効にする](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) および[個々のユーザーの Teams の通知をオンまたはオフにする](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) を参照してください。

2. ユーザーが休暇申請を承認するために使用するのと同じ資格情報で **チャット** タブにログインしていることを確認します。 "サインアウト" というメッセージを使用してから "サインイン" を使用して正しい資格情報でサインインします。

3. それでも問題が解消しない場合は、システム管理者として **ビジネス イベント システム** バッチ ジョブのステータスを確認します。 **待機中** または **実行中** のステージにある場合は、数分後にもう一度戻って確認します。 ステータスが変わらない場合は、弊社のチームで問題を解決することができるように、サポート チケットを記録します。

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
[Teams での休暇要求の管理](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

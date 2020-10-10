---
title: Teams における人事管理アプリ
description: このトピックでは、Microsoft Teams における Microsoft Dynamics 365 Human Resources について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828917"
---
# <a name="human-resources-app-in-teams"></a>Teams における人事管理アプリ

[!include [banner](includes/preview-feature.md)]

Microsoft Teams の Microsoft Dynamics 365 Human Resources アプリを使用すると、従業員は簡単に休暇を申請することができ、Microsoft Teams にて休暇の残日数情報を表示することができます。 従業員は bot と対話して情報を要求できます。 **休暇** タブには、より詳細な情報が表示されます。さらに、Human Resources アプリの外で、チームやチャットで今後の休暇についての情報を送信できます。

![Teams Human Resources の休暇アプリ ボット](./media/hr-admin-teams-leave-app-bot.png)

![Teams Human Resources 休暇アプリの休暇タブ](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources の休暇申請カード](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>インストールと設定

Human Resources アプリは、Teams ストアにあります。 Teams アプリのインストールについては、[Teams で休暇申請を管理する](hr-teams-leave-app.md)を参照してください 。

Teams におけるアプリのアクセス許可の管理については、[Microsoft Teams におけるアプリのアクセス許可ポリシーを管理する](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)を参照してください。

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Teams の Human Resources アプリの通知を有効にする

ユーザーが Teams アプリで休暇申請通知を受け取るようにするには、Human Resources で通知を有効にする必要があります。

>[!NOTE]
>Teams にサインインしていて、Teams の Human Resources アプリを使用しているユーザーだけが、通知を受け取ります。

1. 人事管理では、**システム管理**を選択します。

2. **リンク** を選択します。

3. **設定** で **システム パラメータ** を選択します。

4. **一般** タブで **Teams アプリの通知を有効にする** を **はい** に設定します。

   ![システム パラメータで Teams アプリの通知を有効にする](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. すべてのユーザーに対して Teams の通知をオンにするには、プロンプトで **はい** を選択します。

   ![すべてのユーザーに対して Teams の通知を有効にする](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>個々のユーザーの Teams の通知をオンまたはオフにする

Teams の Human Resources アプリの通知を有効にした後、ユーザーごとに通知をオンまたはオフにすることができます。

1. 人事管理では、**システム管理**を選択します。

2. **リンク** を選択します。

3. **ユーザー** で **ユーザー オプション** を選択します。

4. **ワークフロー** タブを選択します。

5. **Teams アプリの通知を有効にする** を **はい** に設定するとユーザーへの通知が有効になり、**いいえ** に設定するとユーザーへの通知が無効になります。

   ![ユーザー オプションのワークフロー タブで Teams アプリの通知を有効にする](./media/hr-admin-teams-leave-app-notifications.png)

6. **保存** を選択します。

## <a name="known-issues"></a>既知の問題

| 出庫 | ステータス |
| --- | --- |
| Android フォンで水平スクロールが機能しない | 水平スクロールは iOS または デスクトップ デバイスでは問題ではありません。 Android の修正プログラムに取り組んでいます。 |
| 未来日付の休暇を送信する場合に、残日数に誤りがあることを示します。 | 予測機能は未実装です。 現在日付の残日数が表示されます。 |
| **レビュー中**の申請をキャンセルできない 。 | この機能には現在対応していないため、今後のリリースで対応予定です。 |
| 残日数情報が、現日付の時点に基づいて算出される。 | 現在のシステムでは、休暇と欠勤のパラメータで構成されている場合であっても、見越計上期間の残日数は表示されません。 |

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
[Teams での休暇要求の管理](hr-teams-leave-app.md)


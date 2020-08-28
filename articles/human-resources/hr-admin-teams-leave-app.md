---
title: Teams における人事管理アプリ
description: このトピックでは、Microsoft Teams における Microsoft Dynamics 365 Human Resources について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 08/06/2020
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
ms.openlocfilehash: 4822cc6560926df878a8b4e9f821b331ede27a8c
ms.sourcegitcommit: 15c68822f4d412bfc609be31b3702f18c81ea0bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2020
ms.locfileid: "3666363"
---
# <a name="human-resources-app-in-teams"></a>Teams における人事管理アプリ

[!include [banner](includes/preview-feature.md)]

Microsoft Teams の Microsoft Dynamics 365 Human Resources アプリを使用すると、従業員は簡単に休暇を申請することができ、Microsoft Teams にて休暇の残日数情報を表示することができます。 従業員は bot と対話して情報を要求できます。 **休暇** タブには、より詳細な情報が表示されます。

![Teams Human Resources の休暇アプリ ボット](./media/hr-admin-teams-leave-app-bot.png)

![Teams Human Resources 休暇アプリの休暇タブ](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>インストールと設定

Human Resources アプリは、Teams ストアにあります。 Teams アプリのインストールについては、[Teams で休暇申請を管理する](hr-teams-leave-app.md)を参照してください 。

Teams におけるアプリのアクセス許可の管理については、[Microsoft Teams におけるアプリのアクセス許可ポリシーを管理する](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)を参照してください。

## <a name="known-issues"></a>既知の問題

| 出庫 | ステータス |
| --- | --- |
| Android フォンで水平スクロールが機能しない | 水平スクロールは iOS または デスクトップ デバイスでは問題ではありません。 Android の修正プログラムに取り組んでいます。 |
| エラー: 接続する環境の検索に問題があります。 | このエラーは、ユーザーが 1 つ以上の Human Resources 環境にアクセスできることを確認した場合でも、表示されることがあります。 また、予期するすべての環境が表示されない場合があります。 この問題を修正するまでは、ユーザーを削除してから再度インポートして問題を解決してください。 |
| 未来日付の休暇を送信する場合に、残日数に誤りがあることを示します。 | 予測機能は未実装です。 現在日付の残日数が表示されます。 |
| 既存の申請で要した時間数を減らすと、**残日数**が加算されずに減算される。 | この既知の問題については、将来的に対応予定です。 表示内容は正しくありませんが、送信時に正しい日数が調整されます。 |
| **レビュー中**の申請をキャンセルできない 。 | この機能には現在対応していないため、今後のリリースで対応予定です。 |
| 残日数情報が、現日付の時点に基づいて算出される。 | 現在のシステムでは、休暇と欠勤のパラメータで構成されている場合であっても、見越計上期間の残日数は表示されません。 |

## <a name="privacy-notice"></a>プライバシー通知

Microsoft Teams で Dynamics 365 Human Resources Botを使用している場合、ユーザーが入力するテキスト情報は、その基となる問い合わせや意図を理解する目的で分析されます。 ユーザーが入力した 「顧客 Contoso を検索」は、言語理解インテリジェント サービス (LUIS) と呼ばれる、Microsoft の認識サービスの一つにルーティングされます。 LUIS の詳細については、  [こちら](https://www.luis.ai/)を参照してください。 LUIS サービスは、ユーザーによる入力内容の意図 (この場合の意図は情報を見つけること) と対象エンティティ (この場合、意図されたエンティティは Contoso という名前の顧客) の曖昧性を解消した、理解しします。 この情報は、Microsoft の [Azure ボット フレームワーク](https://azure.microsoft.com/services/bot-service/)に渡され、 Dynamics 365 Human Resources のデータと対話し、ユーザーのクエリに必要な情報を取得します。 

ボットをインストールして使用を許可することで、LUIS サービスと Azure ボット フレームワークが入力された内容の意図を処理することに同意したことになります。これによって会話型のユーザーエクスペリエンスが強化されます。 LUIS サービスと Azure ボット フレームワークには、Dynamics 365 Human Resources と比較するとコンプライアンスのレベルが異なる場合があります。 LUIS サービスはユーザーのクエリにしかアクセスできず、ユーザーの Dynamics 365 Human Resources データやアカウントには接続できないように設計されていますが、Dynamics 365 Human Resources ボットのユーザーが自発的に顧客データや個人データなどのデータを含むクエリを入力し、そのクエリの内容が LUIS サービスや Azure ボット フレームワークに送信される可能性があります。 

ユーザーのクエリおよびメッセージの内容は、最大30日間 LUIS システムで保持され、静止時に暗号化されます。トレーニングやサービスの改善に使用されることもありません。 認知サービスの詳細については、 [こちら](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/)を参照してください。 

Microsoft Teams でアプリの管理設定を制御するには、 [Microsoft Teams 管理センター](https://admin.teams.microsoft.com/)に移動してください。 

## <a name="see-also"></a>参照 

[Microsoft Teams のダウンロードとインストール](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams ヘルプ センター](https://support.office.com/teams)</br>
[Teams で休暇申請を管理する](hr-teams-leave-app.md)


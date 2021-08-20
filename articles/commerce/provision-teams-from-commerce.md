---
title: Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング
description: ここでは、Microsoft Teams の組織データを利用して Dynamics 365 Commerce のプロビジョニングを行う方法について説明します。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 715b18acb10edebafe60805393cbc16c5be513ef3605cf7a575ff98362443bb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766436"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング

[!include [banner](includes/banner.md)]

ここでは、Microsoft Teams の組織データを利用して Dynamics 365 Commerce のプロビジョニングを行う方法について説明します。

Dynamics 365 Commerce では、まだ小売店舗にチームを設定していない場合に、簡単に Teams をプロビジョニングすることができます。 Commerce から Teams で使用する情報を活用することで、店舗の従業員が Teams を使い始めることができるようになります。 この情報には、組織階層、店舗名、従業員情報、Azure Active Directory (Azure AD) 勘定などが含まれます。 

Teams の準備のプロセスには、2つの主要な手順があります :

1. Teams では、小売店舗ごとにチームを作成し、店舗の従業員を適切なチームのメンバーとして追加します。 従業員が複数の小売店に関連付けられている場合、その情報がチームのメンバーに反映されます。 各地域のマネージャーをメンバーに加えたコミュニケーション チームを作り、Teams からのタスクの公開を容易にします。
1. Commerc から Teams に組織階層をアップロードします。

## <a name="provision-teams-in-commerce-headquarters"></a>Commerce 本部で Teams をプロビジョンする

Microsoft Teams のプロビジョニングを行う前に、次の作業を行います :

- すべての地域マネージャーがコミュニケーション マネージャーとなっていることを確認します。
- すべての店舗マネージャと従業員の Azure アカウントが Commerce 本部内のマネージャまたは従業員の作業者レコードに関連付けられていることを確認します。

Commerce 本部で Teams をプロビジョニングするには、次の手順に従います。

1. **Retail と Commerce \> チャネル設定 \> Microsoft Teams 統合の構成** に移動します。
1. アクション ペインで、**チームのプロビジョニング** を選択します。 **チームの準備** という名前のバッチ ジョブが作成されます。
1. **システム管理 \> 照会 \> バッチジョブ** に移動し、**Teams のプロビジョニング** の説明がある最新のジョブを検索します。 このジョブの実行が終了するまで待ちます。

> [!TIP]
> 地域マネージャー、店舗マネージャー、店舗従業員のいずれもが Teams のライセンスに関連付けられていない場合、次のエラーメッセージが表示される場合があります : 「ユーザーの適用可能な Sku カテゴリの取得に失敗しました」 この問題を修正するには、アクション ペインの **チームとメンバーの同期** を選択します。

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Teams 管理センターでTeams のプロビジョニングを検証する

Microsoft Teams 管理センターで Microsoft Teams のプロビジョニングを検証するには、次の手順に従います。
    
1. [Teams 管理センター](https://admin.teams.microsoft.com/)に移動し、eコマース テナントの管理者としてログインします。
1. 左ナビゲーション ペインウで、**Teams** を選択して展開し、**チームの管理** を選択します。
1. Commerce の小売店舗ごとにひとつのチームが作成されたことを確認します。
1. チームを選択し、店舗従業員がメンバーとして追加されたことを確認します。
1. 左ナビゲーション ペインで **ユーザー** を選択し、すべての店舗のすべての店舗の従業員がユーザーとして追加されたことを確認します。

次の図は、Teams 管理センターの **チームの管理** ページの例を示しています。

![Teams 管理センターのチームの管理ページの例。](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Commerce の組織階層を Teams にアップロードする
    
Commerce の組織階層を Microsoft Teams で使用すると、同じ階層構造を使用しているすべての店舗または選択した店舗にタスクを発行することができます。

Commerce の組織階層を Teams にアップロードするには、以下の手順で行います。
    
1. Commerce 本部で、**Retail と Commerce \> チャネルの設定 \> Microsoft Teams 統合の構成** の順に移動します。
1. **対象の階層をダウンロード** を選択し、**地域別の小売店舗** を選択して組織階層のコンマ区切り値 (CSV) ファイルをダウンロードします。
1. [Microsoft Teams PowerShell のインストール](/microsoftteams/teams-powershell-install)に記載の手順に従って、Microsoft Teams PowerShell モジュールをインストールします。
1. Teams の PowerShell ウィンドウでプロンプト ウィンドウが表示された場合は、ご利用の Azure AD テナントの管理者アカウントを使用してサインインします。
1. [チームが対象とする階層を設定する](/microsoftteams/set-up-your-team-hierarchy) に記載の手順に従って、対象の階層に CSV ファイルをアップロードします。

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>組織階層が Teams にアップロードされたことを確認する

Microsoft Teams に組織階層がアップロードされたことを確認するには、以下の手順に従います。

1. Teams は通信マネージャーとしてサインインします。
1. 左のナビゲーション ペインで、**Planner によるタスク** を選択します。
1. **公開済 リスト** タブで、ダミーのタスクを含む新しいリストを作成します。
1. **公開** を選択します。 次の図の例のように、**公開対象者** ダイアログ ボックスに組織階層が表示されます。

![公開対象者のダイアログボックスに表示される組織階層の例。](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce と Microsoft Teams データ統合の概要](commerce-teams-integration.md)

[Dynamics 365 Commerce と Microsoft Teams の統合を有効化する](enable-teams-integration.md)

[Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる](synchronize-tasks-teams-pos.md)

[Microsoft Teams でユーザーとロールを管理する](manage-user-roles-teams.md)

[Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします](map-stores-existing-teams.md)

[Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ](teams-integration-faq.md)
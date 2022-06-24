---
title: Microsoft Teams と Dynamics 365 Commerce POS 間でタスク管理を同期させる
description: この記事では、Microsoft Teams と Dynamics 365 Commerce の販売時点管理 (POS) の間で同期する方法について説明します。
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23da56f4f6aee906aad261939d1c7ef9feac5922
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874872"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Microsoft Teams と Dynamics 365 Commerce POS 間でタスク管理を同期させる

[!include [banner](includes/banner.md)]

この記事では、Microsoft Teams と Dynamics 365 Commerce の販売時点管理 (POS) の間で同期する方法について説明します。

Teams 統合の主な目的の1つは、POS アプリケーションとチーム間でのタスク管理の同期を有効に行う目的の1つです。 店舗の従業員は、POS アプリケーションまたはチームを使用してタスクを管理し、アプリケーションを切り替える必要はありません。

Planner はチームのタスクのリポジトリとして使用されるので、Teams と Dynamics 365 Commerce の間にリンクがある必要があります。 このリンクは、特定の店舗チームの特定の計画 ID を使用して作成されます。

次の手順では、POS アプリケーションと Teams アプリケーション間のタスク管理同期を設定する方法を示します。

## <a name="publish-a-test-task-list-in-teams"></a>Teams でのテストタスク リストの公開

次の手順は、店舗チームが初めて Commerce と Microsoft Teams タスク管理統合を使用している場合と仮定しています。

Teams でテスト タスク リストを公開するには、次の手順に従います。

1. Teams は通信マネージャーとしてサインインします。 通常、通信マネージャは、Commerce で **地域マネージャー** ロールを持つユーザーです。
1. 左のナビゲーション ペインで、**Planner によるタスク** を選択します。
1. **発行済みリスト** タブで、左下の **新規リスト** を選択し、新しいリストに **テスト タスク リスト** と指定します。
1. **作成** を選択します。 新しいリストは **ドラフト** の下に表示されます。
1. **タスク タイトル** で、最初のタスクに **Teams 統合のテスト** というタイトルを付けます。 **入力** を選択します。
1. **ドラフト** リストで、タスク リストを選択します。 次に右上隅で  **発行**   を選択します。
1. **発行先の選択** ダイアログ ボックス で、テストタスク リストを受け取るチームを選択します。
1. **次へ** を選択すると、出版物計画が確認されます。 変更する必要がある場合は、 **戻る** を選択します。 
1. **確認を選択して続行** を選択して、**発行** を選択します。
1. 発行が完了した後に、**発行済リスト** タブの上部に表示されるメッセージに、タスク リストが正常に 配信されたかどうかを示します。

詳細については、[組織の作業を作成および追跡するためのタスク リストの公開](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df) を参照してください。

## <a name="link-pos-and-teams-for-task-management"></a>POS とタスク管理のための Teams のリンク

Commerce Headquarters でタスク管理用の POS と Microsoft Teams アプリケーションをリンクするには、次の手順に従います。

> [!NOTE]
> タスク管理を Microsoft Teams に統合する前に、[Dynamics 365 Commerce および Microsoft Teams 統合](enable-teams-integration.md)が有効になっている必要があります。 

1. **小売とコマース \> タスク管理 \> Microsoft Teams とのタスク統合** に移動します。
1. アクション ウィンドウで、**編集** を選択します。
1. **タスク管理統合の有効化** オプションを **はい** に設定します。
1. アクション ウィンドウで、**保存** を選択します。
1. アクション ペインで、**タスク管理の設定** を選択します。 **Teams のプロビジョニング** という名前のバッチ ジョブが作成中であることを示す通知 が表示されます。
1. **システム管理 \> 照会 \> バッチジョブ** に移動し、**Teams のプロビジョニング** の説明がある最新のジョブを検索します。 このジョブの実行が終了するまで待ちます。
1. **CDX ジョブ 1070** を実行して、計画 ID と Retail Server への店舗参照を公開します。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce と Microsoft Teams データ統合の概要](commerce-teams-integration.md)

[Dynamics 365 Commerce と Microsoft Teams の統合を有効化する](enable-teams-integration.md)

[Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング](provision-teams-from-commerce.md)

[Microsoft Teams でユーザーとロールを管理する](manage-user-roles-teams.md)

[Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします](map-stores-existing-teams.md)

[Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ](teams-integration-faq.md)

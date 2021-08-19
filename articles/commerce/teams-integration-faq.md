---
title: Dynamics 365 Commerce と Microsoft Teams の統合に関するよくあるご質問
description: このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams 統合に関連してよく寄せられる質問に対する回答を示します。
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
ms.openlocfilehash: ae4a7f9d9576c9d0408f562eb05bc309d0fbca0ecb8530e8c032b2bb80f12ff4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773817"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Dynamics 365 Commerce と Microsoft Teams の統合に関するよくあるご質問

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams 統合に関連してよく寄せられる質問に対する回答を示します。

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Commerce から Teams を準備する間、店舗内でチームの所有者になるユーザーとは。 

すべての店長は対応するチーム グループに所有者として自動的に追加され、プライベート チャンネルの追加やメンバーの追加や削除などの操作を実行できます。 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Commerce Headquarters で従業員に "通信マネージャ" ロールを割り当てるにはどのようにしますか。 

Microsoft Teams の通信マネージャは、タスク リストを作成および公開できます。 通信マネージャになる必要がある組織の従業員には、Commerce Headquarters で "小売作業マネージャ" ロールが割り当てられている必要があります。

Commerce Headquarters の従業員に小売作業マネージャ ロールを割り当てるには、次の手順に従います。

1. **Retail と Commerce \> 従業員 \> ユーザー** へ移動します。
1. 従業員を選択します。
1. **ユーザーのロール** クイック タブで、**ロールの割り当て** をクリックします。
1. **ユーザーへのロールの割り当て** ダイアログ ボックスで **Retail タスク マネージャー** ロールを選択し、**OK** を選択します。

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>特定の組織階層を Microsoft Teams へアップロード可能にする方法は?

Commerce Headquarters では、すべての組織の階層を 1 つ以上の目的に関連付けることができます。 次の例の図に示すように、Microsoft Teams にプロビジョニングする階層に **Retail レポート** 目的が関連付けられている必要があります。 

![Commerce Headquarters での組織階層の目的の例。](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>小売用店舗の作業者が Azure Active Directory(Azure AD) を使用して販売時点管理 (POS) にログインするにはどのようにしますか 。

Azure AD 認証を使用する Commerce POS のサインイン体験を構成する方法については、[POS サインインの Azure Active Directory 認証を有効にする](aad-pos-logon.md) を参照してください。

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Microsoft Teams の組織でチームを既に作成している場合、Commerce Headquarters で店舗と対応するチームをマップするにはどのようにしますか。

既存のチームがある場合に店舗とチームをマップする方法については、[Microsoft Teams の組織に既存のチームがある場合の、店舗と対応するチームのマップ](map-stores-existing-teams.md) を参照してください。

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>セッション 記憶域に保存されている Microsoft Graph API トークンをクリアする方法は?

Azure Active Directory (Azure AD) アカウントで販売時点管理 POS にログインしたユーザーは、POS からサインアウトするか、アプリケーションを閉じてセッション ストレージ記憶域をクリアする必要があります。 

> [!TIP]
> 推奨されるベスト プラクティスは、常に店舗作業員が POS ターミナルをロックするか、ターミナルを使用しない場合にセッションからサインアウトを行う方法です。 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>店舗に店長がいない場合の方法は?

店舗にマネージャーが存在しない場合、チーム グループは、店舗または Teams に対して作成されません。 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>店舗長が会社を離職した場合の問題は?

所有者ロールを持つユーザーは、Commerce Headquarters で新しい店舗マネージャを追加し、Teams を再プロビジョニングして、グループのチームで必要な権限を新しいマネージャに与えすることができます。 

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce と Microsoft Teams データ統合の概要](commerce-teams-integration.md)

[Dynamics 365 Commerce と Microsoft Teams の統合を有効化する](enable-teams-integration.md)

[Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング](provision-teams-from-commerce.md)

[Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる](synchronize-tasks-teams-pos.md)

[Microsoft Teams でユーザーとロールを管理する](manage-user-roles-teams.md)

[Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします](map-stores-existing-teams.md)

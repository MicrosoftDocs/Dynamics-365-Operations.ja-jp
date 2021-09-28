---
title: サブスクリプションの期限切れとデータ削除
description: このトピックでは、Azure サブスクリプションの有効期限が切れた後に行われるデータの削除に関する情報を提供します。 また、期限切れの Azure サブスクリプションをクリーンアップする方法についても説明します。
author: AngelMarshall
ms.date: 08/16/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2021-08-16
ms.openlocfilehash: 1097c1f237d08fb9d2ce79de976e8fea5cd5e3a4
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441523"
---
# <a name="expired-subscriptions-and-data-deletion"></a>サブスクリプションの期限切れとデータ削除

[!include[banner](../includes/banner.md)]

サブスクリプションの有効期限が切れ 90 日の保持期間を超えた場合、Microsoft はアカウントを無効にし、顧客データを削除します。 Microsoft Dynamics Lifecycle Services (LCS) の実装プロジェクトが削除され、Microsoft が管理する環境がプロビジョニング解除されて削除されます。

## <a name="clean-up-your-azure-subscription"></a>Azure サブスクリプションのクリーンアップ

LCS 実装プロジェクトを削除した後に、顧客所有の Azure サブスクリプションを通じてクラウドでホストされている環境を配置した場合、LCS は Azure サブスクリプションや、クラウドでホストされている環境にはアクセスできなくなります。 ただし、一部のリソースは、Azure サブスクリプションに残っている場合があります。

次の手順に従ってリリースを解放し、Azure Active Directory (Azure AD) テナントおよび以前に LCS に追加した各 Azure サブスクリプションのアプリケーション アクセス許可を削除して、クラウドでホストされる環境を展開できるようにします。

1. Azure リソースの削除:

    1. [Azure ポータル](https://portal.azure.com)で、Azure サブスクリプションにアクセスします。
    1. クラウド ホスト環境が作成されると、その環境は Azure サブスクリプションにリソース グループを作成します。 このリソース グループは、クラウド ホスト環境の配置の一部として作成されたリソースを表します。 配置と同じ名前です。 したがって、リソース グループ一覧を簡単に検索できます。 接頭語 **DynamicsDeployments-** を持つリソース グループを削除します。

    > [!IMPORTANT]
    > クラウド ホスト環境を複数の Azure リージョンに配置した場合は、複数のリソース グループが作成されている可能性があります。 関連するすべてのリソース グループを削除してください。

1. サブスクリプションから配置サービス アプリケーションを削除します。

    1. PowerShell コマンドレットから Azure AD にサインインします。

        ```powershell
        Connect-AzureAD (Using Tenant Administrator account)
        ```

    1. アプリが Azure AD テナントでまだ有効になっているかどうかを確認します。

        ```powershell
        Get-AzureADServicePrincipal -Filter "AppId eq 'b96b7e94-b82e-4e71-99a0-cf7fb188acea'"
        ```

    1. 前述のコマンドがオブジェクトを返す場合、アプリは現在テナントで有効であり、サブスクリプションに引き続きアクセスできる可能性があります。 テナントからアプリを削除します。

        ```powershell
        $DDSObjectId=$(Get-AzureADServicePrincipal -Filter "AppId eq 'b96b7e94-b82e-4e71-99a0-cf7fb188acea'").ObjectId
        ```

        ```powershell
        Remove-AzureADServicePrincipal -ObjectId $DDSObjectId
        ```

    1. アプリが削除されたことを確認してください。

        ```powershell
        Get-AzureADServicePrincipal -Filter "AppId eq ' b96b7e94-b82e-4e71-99a0-cf7fb188acea'"
        ```

## <a name="related-topics"></a>関連トピック

[Microsoft 365 でのデータの保持、削除、破棄](/compliance/assurance/assurance-data-retention-deletion-and-destruction-overview?view=o365-worldwide)

[サブスクリプション、LCS プロジェクト、および Azure Active Directory テナントに関するよく寄せられる質問](../../fin-ops/get-started/subscription-overview.md)

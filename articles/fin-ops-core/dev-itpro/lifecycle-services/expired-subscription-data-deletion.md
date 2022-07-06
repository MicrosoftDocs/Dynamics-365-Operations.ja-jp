---
title: サブスクリプションの期限切れとデータ削除
description: この記事では、Azure サブスクリプションの有効期限が切れた後に行われるデータの削除に関する情報を提供します。 また、期限切れの Azure サブスクリプションをクリーンアップする方法についても説明します。
author: AngelMarshall
ms.date: 08/16/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2021-08-16
ms.openlocfilehash: f2ad0f35b2a39ba3f87d8cc3ba81dfb421b88fad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866454"
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

[Microsoft 365 でデータの保持、削除、破棄](/compliance/assurance/assurance-data-retention-deletion-and-destruction-overview)

[サブスクリプション、LCS プロジェクト、および Azure Active Directory テナントに関するよく寄せられる質問](../../fin-ops/get-started/subscription-overview.md)

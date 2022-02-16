---
title: 認証と承認
description: このトピックでは、財務と運用アプリおよび Microsoft Power Platform 間のユーザー同期およびアクセス許可の認証および承認モデルについて説明します。
author: jaredha
ms.date: 10/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: intro-internal
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-10-14
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: c3c84788e3a2de8ef97448a0739cc8f64c6bee77
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060988"
---
# <a name="authentication-and-authorization"></a>認証と承認

[!include[banner](../includes/banner.md)]



財務と運用アプリおよび Microsoft Power Platform は、個別のユーザー セキュリティを管理します。 ユーザーが Microsoft Power Platform を通して財務と運用アプリのリソースにアクセスするには、各環境で適切なアクセス許可を持っている必要があります。 ユーザー設定は、2 つの環境間でユーザーを同期することで簡略化できます。

## <a name="user-provisioning"></a>ユーザーのプロビジョニング

### <a name="creating-finance-and-operations-apps-users-in-microsoft-power-platform"></a>Microsoft Power Platform で財務と運用アプリのユーザーを作成する

Microsoft Power Platform 環境で財務と運用アプリ ユーザーの作成を自動化する 3 つの方法があります。

- 新しい Microsoft Power Platform 環境が、財務と運用アプリ環境にリンクされたリンク環境として作成されると、Microsoft 365 管理センターで作成され、**Dynamics 365 Finance** ライセンスが割り当てられたすべてのアクティブ ユーザーは、新しい Microsoft Power Platform 環境のユーザーとして自動的に追加されます。 リンクされた環境の作成方法の詳細については、[Microsoft Power Platform 統合の有効化](./enable-power-platform-integration.md) を参照してください。
- Microsoft 365 管理センターに新しいユーザーが作成され、**Dynamics 365 Finance** ライセンスが割り当てられると、新しいユーザーが財務と運用アプリ環境にリンクされる Microsoft Power Platform 環境のユーザーとして自動的に作成されます。 Microsoft Power Platform で新しいユーザーを作成するプロセスには、1 時間ほどかかる場合があります。
- **Dynamics 365 Finance** ライセンスが割り当てられているユーザーがユーザー同期が行われる前に Microsoft Power Platform 環境にサインインするために割り当てられる場合、Microsoft Power Platform 環境に最初にアクセスするときにユーザー レコードが作成されます。

リンクされた Microsoft Power Platform 環境に財務と運用アプリ ユーザーを自動的に作成できます。 ただし、[Dataverse データベースを持つ環境にユーザーを追加する](/power-platform/admin/add-users-to-environment#add-users-to-an-environment-that-has-a-dataverse-database)の手順に従って、財務と運用アプリ ユーザーを直接 Microsoft Power Platform に追加することもできます。

### <a name="creating-microsoft-power-platform-users-in-finance-and-operations-apps"></a>財務と運用アプリで Microsoft Power Platform ユーザーを作成する

管理者は、Azure Active Directory (Azure AD) から財務と運用アプリに Microsoft Power Platform ユーザーを手動でインポートできます。 Azure AD からユーザーをインポートする場合は、財務と運用アプリで **ユーザーのインポート** を選択します。 詳細については、[Azure AD からの新規ユーザーのインポート](../sysadmin/tasks/create-new-users.md#import-new-users-from-azure-ad) を参照してください。

## <a name="security-model"></a>セキュリティ モデル

Dataverse で作業する Microsoft Power Platform ユーザーは、仮想エンティティを通じて財務と運用アプリ エンティティと対話できます。 また、財務と運用アプリのユーザー アクションによってトリガーされたビジネス イベントを受信することもできます。 Dataverse で仮想エンティティと対話するには、仮想エンティティ メタデータへのアクセス権が必要です。 Dataverse でトランザクションが実行される前に、仮想エンティティ呼び出しが財務と運用アプリに対して行われます。 この呼び出しによって、財務と運用アプリで定義されたユーザーのセキュリティ ロールと特権を検証することで、ユーザーの要求が承認されます。

Dataverse 仮想エンティティのインタラクションと財務と運用アプリのセキュリティ モデルの詳細については、[アーキテクチャ](virtual-entities-overview.md#architecture)を参照してください。

### <a name="security-roles-in-microsoft-power-platform"></a>Microsoft Power Platform でのセキュリティ ロール

**Dynamics 365 Finance** ライセンスを持つユーザーが、ユーザーとして Microsoft Power Platform に自動的に作成されると、**Finance and Operations 基本ユーザー** のセキュリティ ロールと **環境メーカー** のセキュリティ ロールの両方が自動的に Microsoft Power Platform ユーザーに割り当てられます。

- **Finance and Operations 基本ユーザー** – このセキュリティ ロールを使用すると、ユーザーは仮想エンティティやビジネス イベントにアクセスして更新できます。 Dataverse 環境で仮想エンティティまたはビジネス イベントが有効化されると、仮想エンティティまたはビジネス イベントの権限がセキュリティ ロールに自動的に付与されます。
- **環境メーカー**- このセキュリティ ロールを使用すると、ユーザーは Power Apps でアプリを作成し、Power Automate でフローします。

Power Platform 管理センターの Microsoft Power Platform ユーザーにセキュリティ ロールを手動で割り当てる方法の詳細については、[ユーザーにセキュリティ ロールを割り当てる](/power-platform/admin/assign-security-roles) を参照してください。

### <a name="security-roles-in-finance-and-operations-apps"></a>財務と運用アプリのセキュリティ ロール

財務と運用アプリでユーザーに割り当てられるセキュリティ ロールは、ユーザーが割り当てられた義務と責務を実行するために必要なシステム アクセス権によって異なります。 財務と運用アプリのセキュリティ ロールは、ユーザーがアクセスできるアプリケーション データを決定します。 財務と運用アプリ内でユーザーに割り当てられたセキュリティ ロールがデータへのアクセス許可を付与しない場合、ユーザーは Microsoft Power Platform 統合を通じてデータにアクセスすることはできません。

財務と運用アプリのセキュリティ ロールは、システム管理者が手動で追加する必要があります。 財務と運用アプリには、異なるセキュリティ ロールを割り当てることができます。

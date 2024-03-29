---
title: インスタンスの削除
description: この記事では、Microsoft Dynamics 365 Human Resources のテスト ドライブ環境または運用環境の削除について説明します。
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178475"
---
# <a name="remove-an-instance"></a>インスタンスの削除

_**適用先:** スタンドアロン インフラストラクチャの人事管理_ 

> [!NOTE]
> 2022 年 7 月から、スタンドアロンの人事管理インフラストラクチャに新しい人事管理環境をプロビジョニングすることはできず、新しい Microsoft Dynamics Lifecycle Services (LCS) プロジェクトを作成することもできません。 顧客は、財務および運用のインフラストラクチャに人事管理の環境を展開することができます。 詳細については、[財務と運用のインフラストラクチャでの人事管理のプロビジョニング](/hr-admin-setup-provision-fo.md)を参照してください。

> [!IMPORTANT]
> 財務と運用アプリのインフラストラクチャは、環境の削除をサポートします。 環境を削除する方法に関する詳細については、[環境の削除](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment)を参照してください。

この記事では、Microsoft Dynamics 365 Human Resources の体験版環境または運用環境の削除について説明します。

## <a name="remove-a-test-drive-environment"></a>テスト ドライブ環境の削除

人事管理のテスト ドライブは、60 日間の有効期限ポリシーでプロビジョニングされます。 ただし、テスト ドライブ環境の所有者には、次の手順に従って早期にトライアルを終了するオプションがあります。 

1. [Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。
2. **環境** を選択します。
3. テスト ドライブ環境を選択します。これには、次のような命名パターンがあります: TestDrive - alias@domain
4. **削除** を選択し、決定内容を確認します。 

既存のテスト ドライブ環境が削除されます。 削除すると、新しいテスト ドライブ環境にサイン アップが可能です。 

## <a name="remove-a-production-environment"></a>運用環境の削除

この記事では、人事管理をクラウド ソリューション プロバイダー (CSP) またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。 

ひとつの人事管理環境がひとつの Power Apps 環境に含まれているため、環境を削除するとき 2 つのオプションを考慮できます。 
- **Power Apps 環境全体の削除** このオプションは、人事管理をプロビジョニングする目的で特別に Power Apps 環境を作成し、実装を開始したばかりの場合、または既存の統合がない場合に優先されます。  
- **人事管理のみを削除します。** このオプションは、Microsoft Power Apps および Power Automate で活用されている豊富なデータが格納された Power Apps 環境が確立されている場合に適しています。


> [!Important]
> Power Apps 環境を削除する前に、それが人事管理の範囲外のデータ統合に使用されていないことを確認してください。 また、既定の Power Apps 環境を削除することはできないので注意してください。 

人事管理や関連付けられたアプリ、およびフローを含む Power Apps 環境全体を削除するには:

1. [Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。
2. **環境** を選択します。
3. 削除する環境を選択してください。
4. **削除** を選択し、決定内容を確認します。 
5. 削除が完了するまで待ちます。
6. 人事管理をサブスクライブするために使用したアカウントを使用して [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) にサインインします。 
7. 環境を含む人事管理プロジェクトを選択します。 
8. LCS プロジェクトでは、**人事管理アプリの管理** タイルを選択します。 
9. 削除するインスタンスを選択します。 
10. **インスタンスの削除** を選択して決定内容を確認します。  

既存の Power Apps 環境から人事管理環境を削除するには、以下の手順を実行します。 人事管理 DevOps チームのサポートおよび連絡を含む必要性が、LCS で直接この機能が有効になるまでの一時的なものであることに注意してください。

1. サポートに連絡し、削除要求を開始してください。
2. サポート チームは、人事管理チームの削除リクエストを開始します。 
3. 環境が削除されたという知らせを受けた後に続行してください。
4. 人事管理をサブスクライブするために使用したアカウントを使用して LCS にサイン インします。 
5. 環境を含む人事管理プロジェクトを選択します。 
6. LCS プロジェクトでは、**人事管理アプリの管理** タイルを選択します。 
7. 削除するインスタンスを選択します。その際、**削除済** の配置ステータスでマークされている必要があります。
8. **インスタンスの削除** を選択して決定内容を確認します。 

## <a name="recover-a-soft-deleted-environment"></a>論理削除された環境を復旧する

人事管理の環境に接続されている Power Apps 環境を削除すると、LCS の人事管理の環境の状態が **論理削除** になります。 この場合、ユーザーは人事に接続することはできません。

環境を復元するには、次の操作を行います :

1. [Power Apps 環境の復旧](/power-platform/admin/recover-environment)の指示に従います。

2. 管理者に連絡して、人事環境を復元してください。 詳細については、[サポート](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照してください。

> [!Warning]
> Power Apps 環境は、削除後の 7 日間のみ保存されています。 この 7 日の期間内に環境を復旧する必要があります。


[!INCLUDE[footer-include](../includes/footer-banner.md)]

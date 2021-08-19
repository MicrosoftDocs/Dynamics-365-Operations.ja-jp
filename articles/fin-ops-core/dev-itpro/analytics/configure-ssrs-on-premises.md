---
title: オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション
description: このトピックでは、オンプレミス配置の SQL Server Reporting Services (SSRS) のコンフィギュレーションに関する情報が提供されます。
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 3853158afdab545dacda996c984b265eb8947db7f90faf80319841eb01c14910
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726360"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション

[!include [banner](../includes/banner.md)]

このトピックの手順を使用して、Microsoft Dynamics 365 Finance + Operations のオンプレミス配置に SQL Server Reporting Services (SSRS) を構成します。

1. SQL Reporting Services Configuration Manager アプリケーションを開きます。
2. **サーバー名** を既定のままにし、現在のコンピューターの名前、および **レポート サーバーのインスタンス**、**MSSQLSERVER** にします。
3. **接続** をクリックします。

    [![サービス コンフィグレーション コネクションのレポート。](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. **サービス アカウント** タブをクリックし、設定が次の図と一致しているかを確認します。

    [![サービス アカウント タブ。](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. **Web サービス URL** タブをクリックし、設定が次の図と一致しているかを確認します。

    [![Web サービス URL タブ。](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. **データベース** タブをクリックし、**データベース名** および **資格情報の設定** が次の図と一致しているかを確認します。

    > [!NOTE]
    > 新しいデータベースを作成する必要があります。 これを行うには **データベースの変更** をクリックし、新しいデータベース名が **DynamicsAxReportServer** であることを確認します。

    [![データベース タブ。](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. **Web ポータル URL** タブをクリックし、設定が次の図と一致しているかを確認します。

    > [!NOTE]
    > **適用** をクリックし、ポータルの作成および適切なコンフィギュレーションを行う必要があります。

    [![Web ポータル URL タブ。](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    ポータルを設定すると、**Web ポータル** タブは次の図と一致するようになります。

    [![Web ポータル タブ。](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. レポートの URL をクリックし、SQL Server Reporting Services web ポータルを表示します。
9. ポータルにアクセスしたら、**Dynamics** という名前の新規フォルダーを作成します。

    [![ダイナミクス フォルダー。](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. **Reporting Services 構成マネージャー** で **電子メール設定** タブをクリックし、設定が次の図に一致しているかを確認します。

    [![電子メール設定タブ。](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. **実行アカウント** タブをクリックし、設定が次の図と一致しているかを確認します。

    [![実行アカウント タブ。](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    **暗号化キー** タブでは既定の設定を変更しません。

    [![暗号化キー タブ。](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. **定期売買の設定** タブをクリックし、設定が次の図と一致しているかを確認します。

    [![定期売買の設定タブ。](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    **スケール アウト配置** タブでは既定の設定を変更しません。

    [![スケール アウト配置タブ。](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    **Power BI 統合** タブで既定の設定を変更しないでください。

    [![Power BI 統合タブ。](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. **終了** をクリックし、**Reporting Services 構成マネージャー** を閉じます。

    [![Reporting Services 構成マネージャーの終了。](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

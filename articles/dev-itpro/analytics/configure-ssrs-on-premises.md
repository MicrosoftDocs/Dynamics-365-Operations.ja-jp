---
title: "オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション"
description: "このトピックでは、オンプレミス配置の SQL Server Reporting Services (SSRS) のコンフィギュレーションに関する情報が提供されます。"
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a1f11641a2ec055cfaa0157ac9a40525daa4006
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション

このトピックの手順を使用し、Microsoft Dynamics 365 for Finance and Operations, Enterprise エディションのオンプレミス配置に SQL Server Reporting Services を構成します。

1. SQL Reporting Services Configuration Manager アプリケーションを開きます。
2. **サーバー名**を既定のままにし、現在のコンピューターの名前、および**レポート サーバーのインスタンス**、**MSSQLSERVER** にします。 
3. **接続** をクリックします。
   
   [![サービス コンフィグレーション コネクションのレポート](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. [サービス アカウント] タブをクリックし、設定が次の図と一致しているかを確認します。

    [![サービス アカウント タブ](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. [Web サービス URL] タブをクリックし、設定が次の図と一致しているかを確認します。 

    [![Web サービス URL タブ](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. [データベース] タブをクリックし、**データベース名**および**資格情報の設定**が次の図と一致しているかを確認します。 **注:** 新しいデータベースを作成する必要があります。 これを行うには [データベースの変更] をクリックし、新しいデータベース名が **DynamicsAxReportServer** であることを確認します。

    [![データベース タブ](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. [Web ポータル URL] タブをクリックし、設定が次の図と一致しているかを確認します。 **注:** [適用] をクリックし、ポータルを作成し、適切に設定する必要があります。

    [![web ポータル url タブ](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
  ポータルを設定すると、[Web ポータル] タブは次の図と一致するようになります。
    [![web ポータル タブ](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. レポートの URL をクリックし、SQL Server Reporting Services web ポータルを表示します。 
9.  ポータルにアクセスしたら、**Dynamics** という名前の新規フォルダーを作成します。

    [![ダイナミクス フォルダー](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. **Reporting Services 構成マネージャー** で [電子メール設定] タブをクリックし、設定が次の図に一致しているかを確認します。

    [![電子メール設定タブ](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. [実行アカウント] タブをクリックし、設定が次の図と一致しているかを確認します。

    [![実行アカウント タブ](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
  [暗号化キー] タブで既定の設定を変更しないでください。[![[暗号化キー] タブ](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. [定期売買の設定] タブをクリックし、設定が次の図と一致しているかを確認します。

    [![定期売買の設定タブ](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
  [スケール アウト配置] タブで既定の設定を変更しないでください。[![[スケール アウト配置] タブ](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
  [Power BI 統合] タブで既定の設定を変更しないでください。[![[Power BI 統合] タブ](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. [終了] をクリックし、Reporting Services 構成マネージャー を閉じます。

    [![reporting services 構成マネージャーの終了](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    



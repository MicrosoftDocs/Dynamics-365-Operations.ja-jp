---
title: ビジネス イベントおよび Azure Service Bus Queue
description: このトピックでは、Microsoft Azure Service Bus Queue エンドポイントの構成方法を説明します。
author: jaredha
ms.date: 11/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-11-03
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6345158ef5f0711f7179c6ff9ddd67ee01c9d54b
ms.sourcegitcommit: f4823a97c856e9a9b4ae14116a43c87f9482dd90
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2021
ms.locfileid: "7779920"
---
# <a name="business-events-and-azure-service-bus-queue"></a>ビジネス イベントおよび Azure Service Bus Queue
[!include[banner](../../includes/banner.md)]

このトピックでは、Microsoft Azure Service Bus Queue エンドポイントの構成方法を説明します。

## <a name="create-an-azure-service-bus-queue-endpoint"></a>Azure Service Bus キュー エンドポイントの作成

1. **ビジネス イベント** ページでは、**エンドポイント** タブで、**新規** を選びエンドポイントを作成します。
2. **新しいエンドポイントの構成** ダイアログ ボックスでは、**エンドポイント型** フィールドにて適切なエンドポイント型を選択します。 Service Bus キューにエンドポイントを作成するには、**Azure Service Busキュー** を選択します。
3. **次へ** を選択します。

    ![新しいエンドポイント ダイアログ ボックスの構成のエンドポイント型として Azure Service Bus Queue を選択します。](../../media/businesseventsnewendpoint1.png)

4. **エンドポイント名** フィールドで、エンドポイント名を入力します。
5. Azure Key Vault を設定し、Azure メッセージング リソースにシークレットを提供します。
6. Azure Active Directory (Azure AD) アプリケーション ID およびアプリケーション シークレットを設定します。
7. **新しいエンドポイントの構成** ダイアログ ボックスに戻り、**Queue 名** フィールドにて、Azure の Azure Service Bus Queue 構成にある Service Bus キュー用に作成した名前を入力します。

    ![Azure の Azure Service Bus Queue 構成で作成した Service Bus Queue 名。](../../media/BusinessEventsSBQueueName.PNG)

8. **Azure Active Directory アプリケーション ID** フィールドに、Azure ポータルの Azure AD で作成したアプリケーション ID を入力します。

    ![Azure ポータル内の Azure AD アプリケーション ID。](../../media/businesseventsaad1.png)

9. **Azure アプリケーション シークレット** フィールドに、アプリケーションのシークレット値を入力します。

    ![Azure ポータル内のアプリケーション用シークレット値。](../../media/businesseventsaad2.png)

10. **Key Vault DNS 名** フィールドに、Key Vault 設定から ドメイン名システム (DNS) の名前を入力します。

    ![Key Vault 設定から DNS 名。](../../media/businesseventskeyvault1.png)

11. **Key Vault シークレット名** フィールドに、Key Vault に作成する必要があるエンドポイント リソースのシークレット名を入力します。

    ![Key Vault で作成する必要があるエンドポイント リソースのシークレット名。](../../media/businesseventskeyvault2.png)

    Azure の **Key Vault Secret** 値は、Service Bus 用の **プライマリ接続文字列** 値になります。 **Shared Access Policies \> RootManagedSharedAccessKey** にて、構成した Service Bus の値を確認できます。

    ![ビジネス イベントの Key Vault のキー値。](../../media/BusinessEventsKVSValue.PNG)

12.  **OK** を選択します。

    ![新しいエンドポイント ダイアログ ボックス構成のエンドポイント名と Service Bus キューを選択します。](../../media/businesseventsnewendpoint2.png)

> [!IMPORTANT]
> また、登録された Azure アプリケーションは、キー値の **アクセス ポリシー** で設定された Key Vault に追加する必要があります。 この設定を完了するには、**キー、シークレット、および証明書の管理** テンプレートを選択し、アプリケーションを **プリンシパル** として選択します。

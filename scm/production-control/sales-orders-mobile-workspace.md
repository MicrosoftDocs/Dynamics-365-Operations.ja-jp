---
title: "Microsoft Dynamics 365 for Operations アプリケーションの販売注文モバイル ワークスペース"
description: "販売注文モバイル ワークスペースを使用すると、どこでも、いつでも販売注文を最新の状態に保つことができます。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Microsoft Dynamics 365 for Operations アプリケーションの販売注文モバイル ワークスペース

販売注文モバイル ワークスペースを使用すると、どこでも、いつでも販売注文を最新の状態に保つことができます。 

<a name="prerequisites"></a>必要条件
-------------

| 前提条件                                                         | 説明                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft Dynamics 365 for Operations モバイル プラットフォームについての確認 | [Dynamics 365 for Operations モバイル プラットフォーム](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Microsoft Dynamics 365 for Operations バージョン 1611 および Microsoft Dynamics for Operations プラットフォーム更新プログラム 3 (2016 年11 月) がある環境を使用していることを確認します。 |
| 修正プログラム KB 3215650                                                     | Microsoft Dynamics 365 for Operations で提供されるワークスペースを有効にするように修正プログラムをインストールします。                                                                       |
| Dynamics 365 for Operations アプリがインストールされたモバイル デバイス | モバイル アプリ ストアで、Dynamics 365 for Operations アプリをダウンロードします。                                                                                                      |

## <a name="overview"></a>概要
このモバイル ワークスペースは、Dynamics 365 for Operations アプリケーションにアクセスして、注文ステータス、顧客の連絡先情報および注文受付者の連絡先情報など、各販売注文の詳細情報を表示できるようになります。 モバイル ワークスペースは、販売注文のインスタント ビューを提供します。 顧客別の販売注文、すべての販売注文、または特定の販売注文に関する情報を表示できます。 モバイル ワークスペースは、より詳しい販売注文の分析に役立つ 2 つのビューを提供します。

### <a name="view-all-sales-orders"></a>すべての販売注文の表示

このビューは、すべての販売注文を一覧表示します。

-   表示する販売注文を選択するため、次のフィルターの 1 つを使用します。
    -   販売注文で検索
    -   顧客 ID で検索
    -   顧客名で検索
    -   ステータスで検索
    -   リリース状態で検索
    -   作成日時で検索

<!-- -->

-   販売注文を選択したのち、特定の注文の詳細を表示できます。 具体的には、次の点を表示できます。
    -   顧客の名前と住所情報
    -   指定出荷日および確定出荷日などの、異なる販売注文日
    -   注文受付者の連絡先情報
    -   顧客の連絡先情報
    -   注文明細行
    -   販売注文がいつどのように出荷されたかを示す出荷

### <a name="view-orders-for-a-customer-"></a>顧客の注文を表示します** **　

顧客ごとの販売注文の一覧を表示します。

-   顧客の注文を表示するため、次のフィルターの 1 つを使用します。
    -   名前で検索
    -   ID で検索

<!-- -->

-   顧客を選択したのち、次のものを表示できます。
    -   顧客名およびグループ
    -   顧客の連絡先情報
    -   顧客の販売注文および販売注文に関する詳細。
        -   顧客の名前と住所情報
        -   異なる販売注文日
        -   注文受付者の連絡先情報
        -   顧客の連絡先情報
        -   注文明細行
        -   販売注文がいつどのように出荷されたかを示す出荷

## <a name="get-started"></a>はじめに
モバイル デバイスで販売注文モバイル ワークスペースを使用するには、次の手順に従います。

1.  携帯電話アプリケーションの店舗で、Microsoft Dynamics 365 for Operations アプリケーションをダウンロードおよびインストールします。
2.  デバイスでアプリを起動します。
3.  Dynamics 365 の URL を入力します。
4.  サインインする会社を入力します。 たとえば、「**USMF**」と入力します。
5.  初回サインイン時、Microsoft Dynamics 365 for Operations のユーザー名とパスワードの入力を求められます。 資格情報を入力します。 サインインすると、会社の使用できるワークスペースが表示されます。

モバイル アプリでワークスペースを表示するには、まず Dynamics 365 for Operations アプリに対象のワークスペースを公開する必要があります。

1.  Dynamics 365 for Operations を起動します。
2.  [**システム管理**] &gt; [**設定**] &gt; [**システム パラメーター**] の順に移動します。
3.  [**モバイル アプリの管理**] を選択します。
4.  モバイル プラットフォームを公開するワークスペースを選択します。
5.  **ワークスペースの公開**を選択します。
6.  公開されたワークスペースを表示するデバイスを更新します。

## <a name="view-information-about-sales-orders-for-a-customer"></a>顧客に対する販売注文についての情報を表示します。
1.  モバイル デバイスで、**販売注文** ワークスペースを選択します。
2.  **顧客の注文の表示**を選択します。
3.  必要な顧客を見つけるため **アカウント **または **顧客名 **情報を使用します。
4.  顧客を選択します。
5.  **連絡先情報** または **販売注文**を選択します。
6.  **販売注文** がオンになっていると、顧客の販売注文の一覧が表示されます。
7.  **販売注文**を選択します。
8.  ここで販売注文明細行、出荷、顧客の連絡先情報、および注文受付者の連絡先情報を表示できます。





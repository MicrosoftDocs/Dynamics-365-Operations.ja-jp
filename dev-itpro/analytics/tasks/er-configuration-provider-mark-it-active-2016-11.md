--- 
title: "コンフィギュレーション プロバイダーを作成し、電子申告 (ER) が有効なプロバイダーとしてマーク付けする"
description: "次の手順では、システム管理者または電子レポート開発者に割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 17d0653890236ba5517b854088c04ea7db2593d7
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a>コンフィギュレーション プロバイダーを作成し、電子申告 (ER) が有効なプロバイダーとしてマーク付けする

[!include[task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子レポート開発者に割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法を説明します。 各 ER コンフィギュレーションは、コンフィギュレーションの作成者としてプロバイダーを参照するようになります。 この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行されます。


## <a name="create-a-provider"></a>プロバイダーの作成
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーション プロバイダー] をクリックします。
3. [新規] をクリックします。
    * プロバイダー レコードには固有の名称とURL があります。 このページの内容を確認し、Litware, Inc. (http://www.litware.com) のレコードがすでに存在する場合、この手順をスキップします。  
4. [名前] フィールドに「Litware, Inc.」を入力します。
    * Litware, Inc.  
5. [インターネット アドレス] フィールドに「http://www.litware.com」を入力します。
    * http://www.litware.com  
6. [保存] をクリックします。
7. ページを閉じます。

## <a name="select-as-an-active-provider"></a>有効なプロバイダーとして選択する
1. Litware, Inc. を選択して プロバイダー
2. [有効に設定] をクリックします。



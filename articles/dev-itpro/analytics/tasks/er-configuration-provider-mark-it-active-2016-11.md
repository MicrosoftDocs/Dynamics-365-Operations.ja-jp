--- 
title: "コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け"
description: "次の手順では、システム管理者または電子レポート開発者に割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 37957f224cb57fd9f6c5014740bcea124a99a03a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け

[!include [task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子レポート開発者に割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法を説明します。 各 ER コンフィギュレーションは、コンフィギュレーションの作成者としてプロバイダーを参照するようになります。 この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行されます。


## <a name="create-a-provider"></a>プロバイダーの作成
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [コンフィギュレーション プロバイダー] をクリックします。
3. [新規] をクリックします。
    * プロバイダー レコードには固有の名称とURL があります。 このページの内容を確認し、Litware, Inc. (`http://www.litware.com`) の記録が既に存在している場合、この手順を省略します。  
4. [名前] フィールドに「Litware, Inc.」を入力します。
    * Litware, Inc.  
5. [インターネット アドレス] フィールドに `http://www.litware.com`を入力します。
6. [保存] をクリックします。
7. ページを閉じます。

## <a name="select-as-an-active-provider"></a>有効なプロバイダーとして選択する
1. Litware, Inc. を選択して プロバイダー
2. [有効に設定] をクリックします。



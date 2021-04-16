---
title: コンフィギュレーション プロバイダーを作成し、有効としてマークする
description: このトピックでは、システム管理者または電子申告開発者のロールに割り当てられたユーザーが、コンフィギュレーション プロバイダーを作成する方法について説明します。
author: NickSelin
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27e1275199d098fffb56db61ed6bfd2fc3cdb790
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755133"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>コンフィギュレーション プロバイダーを作成し、有効としてマークする

[!include [banner](../../includes/banner.md)]

このトピックでは、システム管理者または電子レポート開発者のロールに割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法について説明します。 各 ER コンフィギュレーションは、コンフィギュレーションの作成者としてプロバイダーを参照するようになります。 この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行されます。

## <a name="create-a-provider"></a>プロバイダーの作成
1. 左上隅の **ナビゲーション ウィンドウ** に移動して、**組織管理** を選択します。
2. **ワークスペース > 電子申告** に移動します。
3. **関連リンク > コンフィギュレーション プロバイダー** に移動します。
4. **新規** を選択します。
    - プロバイダー レコードには固有の名称とURL があります。 このページの内容を確認し、Litware, Inc. (https://www.litware.com) の記録が既に存在している場合、この手順を省略します。  
5. 名前フィールドに、`Litware, Inc.` と入力します。
6. インターネット アドレス フィールドに `https://www.litware.com` と入力します。
7. **保存** を選択します。
8. ページを閉じます。

## <a name="select-as-an-active-provider"></a>有効なプロバイダーとして選択する
1. Litware, Inc. を選択して プロバイダー
2. **有効に設定** を選択します。

![電子申告ワークスペース ページ](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
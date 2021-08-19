---
title: RCS からの (ER) インポート構成
description: このトピックでは、ユーザーが RCS から ER 構成の新しいバージョンをインポートする方法を説明します。
author: NickSelin
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5674c418baaac7817c27780e2f0137ce6e7137eb3f1665f768ad843cc5b3114
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720787"
---
# <a name="er-import-configurations-from-rcs"></a>RCS からの (ER) インポート構成

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者または電子申告開発者ロールのユーザーが、Microsoft Regulatory Configuration Services (RCS) から新しいバージョンの電子申告 (ER) 構成をインポートする方法を説明します。 この例では、RCS インスタンスで構成されている ER 構成のバージョンを選択して、Litware, Inc. というサンプル企業の現在のインスタンスにインポートします。ER 構成は会社間で共有されるため、これらの手順はすべての会社で実行できます。 これらの手順を完了するには、まず [コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) のトピックにある手順を完了する必要があります。 これらの手順を完了するには、**完了** または **共有** のステータスを持つ 1 つ以上の ER 構成を含む RCS インスタンスへのアクセスも必要です。

1. **組織管理** > **ワークスペース** > **電子申告** の順に移動します。 
2. サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ** としてマークされていることを確認します。 このコンフィギュレーション プロバイダーが表示されない場合、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) というトピックの手順を完了する必要があります。 
3. RCS 環境が自分の会社にプロビジョニングされていない場合は、外部リンク **Regulatory services – 構成** をクリックして、RCS 環境をプロビジョニングする指示に従います。 
4. **電子申告のパラメーター** を選択します。 
5. **RCS** タブをクリックします。 
6. RCS 環境がすでに会社にプロビジョニングされている場合、表示されているページの URL を使ってアクセスします。 
7. ページを閉じます。 

## <a name="register-a-new-er-repository"></a>新しい ER リポジトリを登録します。 
1. 一覧で、選択された行をマークします。 
2. Litware, Inc. プロバイダーを選択します。 
3. リポジトリ を選択します。 
4. 追加を選択してドロップ ダイアログを開きます。 
5. 構成リポジトリ タイプ フィールドで 'RCS' と入力します。 
6. レポジトリを作成を選択します。 
7. RCS 環境表示名フィールドで値を入力または選択します。 
8. 目的の RCS インスタンスを選択します。 複数のインスタンスがあることに注意してください。 
9. OK を選択します。 

## <a name="import-er-configurations-from-rcs-based-repository"></a>RCS ベースのリポジトリからの ER 構成のインポート
1. **フィルタの表示** を選択します。 
2. **次の値で始まる** フィルター演算子を使用して、**名前** フィールドにフィルター値 "RCS" を入力します。 
3. 選択したリポジトリを開くには、**Regulatory Configuration Services への接続** ページで、**Regulatory Configuration Services に接続するには、ここを選択** のリンクを選択します。 
4. **開く** を選択します。 
5. **閉じる** を選択します。 
6. ER 構成の目的のバージョンを選択、**インポート** を選択し、そのバージョンを現在のインスタンスにインポートします。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
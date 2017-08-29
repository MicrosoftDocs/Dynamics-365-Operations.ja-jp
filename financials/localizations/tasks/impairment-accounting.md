--- 
title: "減損会計の共通パラメーターおよび転記プロファイルの設定 (日本)"
description: "このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4a58488e20a6c37c7d258546c61d170b5db43d84
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-impairment-accounting-common-parameters-and-posting-profile-japan"></a>減損会計の共通パラメーターおよび転記プロファイルの設定 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順では、JPMF デモ会社のデータを使用します。


## <a name="set-up-impairment-parameters"></a>減損パラメーターを設定
1. [固定資産] > [設定] > [固定資産パラメーター] の順に移動します。
2. [減損管理] セクションを展開します。
3. [警告期間 (月数) ] フィールドに、数値を入力します。
    * 例: 6 か月  
4. [番号順序] タブをクリックします。
    * 次の番号順序コードが設定されていることを確認します: •減損のドキュメント ID •減損テスト ID •キャッシュ生成単位番号 

## <a name="set-up-posting-profile"></a>転記プロファイルを設定
1. [固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。
2. [編集] をクリックします。
3. [減損管理] セクションを展開します。
4. [追加] をクリックします。
5. [帳簿] フィールドに値を入力します。
6. [グループ化] フィールドで、オプションを選択します。
7. [固定資産番号] フィールドに値を入力します。
8. [主勘定] フィールドに、目的の値を指定します。
9. [相殺勘定] フィールドで、任意の値を指定します。
10. [保存] をクリックします。



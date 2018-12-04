--- 
title: "減損会計の共通パラメーターおよび転記プロファイルの設定"
description: "このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetParameters, AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f5bf676d03d5561d26ce84bbf64010e321725a49
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="setup-impairment-accounting-common-parameters-and-posting-profile"></a>減損会計の共通パラメーターおよび転記プロファイルの設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
    *   

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



---
title: 減損会計の共通パラメーターおよび転記プロファイルの設定
description: このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。
author: kfend
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: AssetParameters, AssetPosting
ms.openlocfilehash: 7677158ebd879e8b345d7869db90910c1857994b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285734"
---
# <a name="setup-impairment-accounting-common-parameters-and-posting-profile"></a>減損会計の共通パラメーターおよび転記プロファイルの設定

[!include [banner](../../includes/banner.md)]

このタスクでは、減損会計の共通パラメーターと転記プロファイルの定義方法が確認できます。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順では、JPMF デモ会社のデータを使用します。


## <a name="set-up-impairment-parameters"></a>減損パラメーターを設定
1. [固定資産] > [設定] > [固定資産パラメーター] の順に移動します。
2. [減損管理] セクションを展開します。
3. [警告期間 (月数) ] フィールドに、数値を入力します。
    * 例: 6 か月  
4. 番号順序タブをクリックし、次の番号順序コードが設定されていることを確定します。  
 - 減損のドキュメント ID
 - 減損損失テスト ID
 - 資産グループ番号        

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

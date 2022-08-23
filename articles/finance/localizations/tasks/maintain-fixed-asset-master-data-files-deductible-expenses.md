---
title: 損金の固定資産マスター データ ファイルの管理
description: このタスクでは、損金の固定資産マスター データの保守を行います。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- AssetGroup, AssetGroupBookSetup
- AssetTable, AssetBook
ms.openlocfilehash: 90eda33b895644d473de0e7a41f09f04535b27e7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270556"
---
# <a name="maintain-fixed-asset-master-data-files-for-deductible-expenses"></a>損金の固定資産マスター データ ファイルの管理

[!include [banner](../../includes/banner.md)]

このタスクでは、損金の固定資産マスター データの保守を行います。



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="setups-in-fixed-asset-groups"></a>固定資産グループの設定
1. [固定資産] > [設定] > [固定資産グループ] の順に移動します。
2. [新規] をクリックします。
3. [固定資産グループ] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
5. [固定資産の自動採番] フィールドで、[はい] を選択します。
6. 番号順序コードを選択して、固定資産番号を自動生成します。
7. 新しい固定資産の既定の場所を選択します。
8. [帳簿] をクリックします。
9. [新規] をクリックします。
10. [帳簿] フィールドに値を入力します。
    * 例: 200RED_CUR  
11. [一般] セクションを展開します。
    * オプションをコンフィギュレーションします。  
    * 各オプションの詳細については、他の情報を参照してください。  
12. [保存] をクリックします。
13. [新規] をクリックします。
14. [帳簿] フィールドに値を入力します。
    * 例: 250NDB_TAX  
15. [一般] セクションを展開します。
    * オプションをコンフィギュレーションします。  
    * 各オプションの詳細については、他の情報を参照してください。  
16. [保存] をクリックします。

## <a name="creation-of-fixed-asset"></a>固定資産の作成
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. [新規] をクリックします。
3. [固定資産グループ] フィールドに値を入力します。
    * 作成した固定資産グループを使用するか、BUIL-M を使用できます。  
4. [帳簿] をクリックします。
    * 帳簿が自動的に作成されたことを確認します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

--- 
title: "損金の固定資産マスター データ ファイルの保守 (日本)"
description: "このタスクでは、損金の固定資産マスター データの保守を行います。"
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
ms.openlocfilehash: db6c04b4bf29d21bb57e3c815278999a207853a3
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="maintain-fixed-asset-master-data-files-for-deductible-expenses-japan"></a>損金の固定資産マスター データ ファイルの保守 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

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



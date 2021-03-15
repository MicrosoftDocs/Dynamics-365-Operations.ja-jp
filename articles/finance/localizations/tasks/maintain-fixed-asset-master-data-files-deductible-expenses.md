---
title: 損金の固定資産マスター データ ファイルの管理
description: このタスクでは、損金の固定資産マスター データの保守を行います。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup,  AssetTable, AssetBook
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12495935ab617bb0526aa790225f6ee7bb804a38
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997438"
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
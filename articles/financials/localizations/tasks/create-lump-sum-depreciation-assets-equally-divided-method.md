--- 
title: "均等償却を使用した一括比例配分減価償却資産の作成 (日本)"
description: "日本では、耐用年数期間中、毎年均等額で減価償却処理される固定資産のタイプが 3 つあります。"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: e616a35758f2dd8622ac1c210c9cc5d615210aca
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-lump-sum-depreciation-assets-using-equally-divided-method-japan"></a>均等償却を使用した一括比例配分減価償却資産の作成 (日本)

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、耐用年数期間中、毎年均等額で減価償却処理される固定資産のタイプが 3 つあります。 その 3 つのタイプとは、一括比例配分資産、繰延資産、および低価額資産です。 



このタスクでは、一括比例配分の固定資産の作成方法について説明します。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順では、JPMF デモ会社のデータを使用します。


## <a name="create-a-lumpsum-fixed-asset"></a>一括比例配分固定資産の作成
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. [新規] をクリックします。
3. [固定資産グループ] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
    * [タイプ] の規定値が [固定資産グループ] により設定されていることを確認します。   
    * [繰延資産] の [繰延タイプ] を設定します。  
    * [資産分類] が [一括比例配分] に設定されていることを確認します。  
    * 低価額資産の [低価額] に対する [資産分類] を設定します。  
5. [保存] をクリックします。
6. [帳簿] をクリックします。
7. [減価償却] セクションを展開します。
    * [方法] が [均等] であることを確認します。  

## <a name="confirm-the-depreciation-profile"></a>減価償却プロファイルの確認
1. [固定資産] > [設定] > [減価償却プロファイル] に移動します。
2. [クイック フィルター] を使用して、[減価償却プロファイル] フィールドで「LUMPSUM」という値を指定してフィルターを実行します。
    * [方法] が [均等] であることを確認します。  
    * [均等償却年数] が 3 年であることを確認します。  
    * この値は、固定資産のタイプが一括比例配分か、繰延資産か、または低価額資産かによって異なります。  



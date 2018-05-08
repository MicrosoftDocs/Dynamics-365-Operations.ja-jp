--- 
title: "特別償却プロファイルのある固定資産の作成 (日本)"
description: "日本では、特定の条件下で特別償却額を固定資産に転記できます この手順を使用して、特別償却プロファイルのある固定資産の作成方法を説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: a1c4b7623f3409d4474adcd04fb1331b944b9fbb
ms.openlocfilehash: e102148545435f63af1c559512fca408805ad1a8
ms.contentlocale: ja-jp
ms.lasthandoff: 02/13/2018

---
# <a name="create-a-fixed-asset-with-special-depreciation-profile-japan"></a>特別償却プロファイルのある固定資産の作成 (日本)

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、特定の条件下で特別償却額を固定資産に転記できます



この手順を使用して、特別償却プロファイルのある固定資産の作成方法を説明します。



この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順では、JPMF デモ会社のデータを使用します。

1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. [新規] をクリックします。
3. [固定資産グループ] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
5. [保存] をクリックします。
6. [価値モデル] をクリックします。
7. [減価償却] セクションを展開または折りたたみます。
    * 特別減価償却プロファイルとして [特別償却プロファイル] を選択します。  
    * EQUP-M と 200NDB_CSR には、すでに既定のコンフィギュレーションとしてデモ データに SpeRE-1M があることに注意してください。  
    * [取崩開始]、[取崩基準]、および[取崩期数] には既定が入力されます。 これらは必要に応じて変更できます。 これらは特別減価償却の引当メソッド固有のものです。  



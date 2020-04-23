---
title: 品目再配賦の未処理ピッキングの設定
description: この手順では、指定された場所に在庫が不十分な場合、倉庫作業者が他の倉庫を素早く見つけることができる方法について説明します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e860a54c2306f8140947b77cdcb538160a84e06f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216810"
---
# <a name="set-up-short-picking-item-reallocation"></a>品目再配賦の未処理ピッキングの設定

[!include [banner](../../includes/banner.md)]

この手順では、指定された場所に在庫が不十分な場合、倉庫作業者が他の倉庫を素早く見つけることができる方法について説明します。 他の場所に製品がある場合、その製品を取得するために場所のディレクティブを使用する、自動再配分プロセスを使用することもできます。 また手動再配分を行う場合、有効数量の対応が可能な場所の一覧がモバイル端末に表示され、これにより倉庫従事者は在庫にはどの場所がよいか選択することができます。 デモ データの会社 USMF でこの手順を使用できます。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="set-up-work-exceptions"></a>作業例外を設定します
1. **ナビゲーション ウィンドウ**で、**倉庫管理 > 設定 > 作業 > 例外作業**の順に移動します。
2. **新規** をクリックします。 倉庫作業者が処理している出荷のニーズに基づいて選択を行えるように、異なる品目の再配置ポリシーでいくつかの作業の例外を定義することができます。  
3. **例外作業コード** フィールドで、値を入力します。 例外作業の使途がわかるようにタイトルを付けます。 たとえば、ショートピッキングに関するマニュアルなど。  
4. **説明**フィールドで、値を入力します。
5. **例外**タイプのフィールドで、「ショートピック」を選択します。 
6. **在庫調整**チェック ボックスを選択します。 このオプションでは、在庫が簡単なピッキング場所の0に自動的に調整されます。  
7. **既定の調整タイプ コード** フィールドで、値を入力または選択します。 たとえば、USMFでは「 Res Adj Outを削除」を選択できます。  
8. **品目再配置**フィールドで、「手作業」を選択します。 手動または自動および手動を選択した場合、倉庫従事者は手動での再配分を実行できなければなりません。  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>手作業による品目再配分を使用する作業者を設定します。
1. ページを閉じます。
2. **ナビゲーション ウィンドウ**で、**倉庫管理 > 設定 > 作業者**の順に移動します。
3. **編集** をクリックします。
4. リストで、[作業者 24] を選択します。
5. **作業**クイック タブを展開します。
6. **手動による再配置を許可**のフィールドで 「はい」を選択します。


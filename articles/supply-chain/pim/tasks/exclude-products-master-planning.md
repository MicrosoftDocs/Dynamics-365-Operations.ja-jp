---
title: マスター プランから製品を除外する場合は、製品ライフサイクルの状態を作成
description: この手順では、マスター プランおよび BOM レベルの計算から製品を除外する新製品ライフサイクルの状態を作成する方法を示します。
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f9573fd220cd8b6a58f81e4d17ca65234f41beb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431822"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>マスター プランから製品を除外する場合は、製品ライフサイクルの状態を作成

[!include [banner](../../includes/banner.md)]

この手順では、マスター プランおよび BOM レベルの計算から製品を除外する新製品ライフサイクルの状態を作成する方法を示します。


## <a name="create-an-obsolete-state"></a>古い形式の状態を作成します
1. [製品情報管理] > [設定] > [製品ライフサイクルの状態] の順に移動します。
2. [新規] をクリックします。
3. [状態] フィールドに値を入力します。
4. [計画に対して有効] フィールドで [いいえ] を選択します。
5. [説明] フィールドに値を入力します。

## <a name="associate-the-obsolete-state-to-a-released-product"></a>リリース済製品に古い形式の状態を関連付ける
1. ページを閉じます。
2. [製品情報管理] > [製品] > [リリースされた製品] の順に移動します。
3. クイック フィルターを使用して、レコードを見つけます。 たとえば、「M00」という値を含む [検索名] フィールドをフィルター処理します。
4. [編集] をクリックします。
5. 一覧で、選択された行をマークします。
6. [製品ライフサイクルの状態] フィールドで値を入力または選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
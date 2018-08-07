--- 
title: "製品ライフサイクルの状態をリリース済製品マスターに割り当て"
description: "ここでは、リリースされた製品およびそのバリアントに、製品ライフサイクルの状態を割り当てる手順を説明します。"
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: f476c1b2585ce0b5b67cd0d91684c86f7d3bda36
ms.contentlocale: ja-jp
ms.lasthandoff: 02/08/2018

---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>製品ライフサイクルの状態をリリース済製品マスターに割り当て

[!include [task guide banner](../../includes/task-guide-banner.md)]

ここでは、リリースされた製品およびそのバリアントに、製品ライフサイクルの状態を割り当てる手順を説明します。 前提条件: まずタスク ガイド「新しい製品のライフサイクルの状態の作成」を実行し、このタスク ガイドを実行する前に作成された、少なくとも 1 つの製品ライフサイクルの状態があることを確認する必要があります。


## <a name="find-a-released-product-master"></a>リリース済製品マスターを検索します。
1. [製品情報管理] > [製品] > [リリースされた製品] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。

> [!NOTE]
> 製品マスターには、製品サブタイプの製品マスターがあります。  

## <a name="update-the-lifecycle-state"></a>ライフサイクルの状態を更新します。
1. [編集] をクリックします。
2. [製品ライフサイクルの状態] フィールドで値を入力または選択します。
3. [保存] をクリックします。
4. [はい] をクリックします。

> [!NOTE]
> [はい] を選択した場合、リリースされた製品マスターとして同じ元のステータスを持つ関連するすべてのリリースされた製品バリアントは、新製品ライフサイクルの状態にも更新されます。 [いいえ] を選択した場合、すべてのバリアントは実際の状態を保持します。 リリースされた製品マスターから別の製品ライフサイクルの状態を持つバリアントは、更新されません。  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>バリアントのライフサイクルの状態を確認します。
1. [リリース済製品バリアント] をクリックします。

> [!NOTE]
> すべてのバリアントが、リリースされた製品マスターから選択済ライフサイクルの状態を継承したことに注意してください。  

2. 一覧で、選択された行をマークします。
3. [製品ライフサイクルの状態] フィールドで値を入力または選択します。



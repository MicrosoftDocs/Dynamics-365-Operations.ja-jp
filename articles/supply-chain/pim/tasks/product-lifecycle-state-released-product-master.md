---
title: 製品ライフサイクルの状態をリリース済製品マスターに割り当て
description: ここでは、リリースされた製品およびそのバリアントに、製品ライフサイクルの状態を割り当てる手順を説明します。
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
ms.openlocfilehash: 2c644f118e0bdb46b296cec7e4a3ea89031f2d52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431816"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>製品ライフサイクルの状態をリリース済製品マスターに割り当て

[!include [banner](../../includes/banner.md)]

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


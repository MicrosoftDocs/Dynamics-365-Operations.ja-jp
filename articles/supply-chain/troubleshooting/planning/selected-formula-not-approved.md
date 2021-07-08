---
title: 選択したフォーミュラ番号がバッチ オーダーに対して承認されていない場合
description: 計画オーダーを確定しようとすると、選択したフォーミュラ番号がバッチ オーダーに対して承認されていないことを示すエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294115"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>選択したフォーミュラ番号がバッチ オーダーに対して承認されていない場合

エラーコード: PRO2614

## <a name="symptoms"></a>現象

計画オーダーを確定しようとする際に、次のエラー メッセージが表示されます:

> 選択したフォーミュラ番号は、オーダー (バッチ) に承認されていません。

## <a name="cause"></a>原因

システムは、確定操作を検証して、承認済みのフォーミュラが有効な品目に使用できることを確認します。 数式を承認することが必要となる場合があります。

## <a name="resolution"></a>解決策

フォーミュラを承認するには、次の手順を実行します。

1. **製品情報管理 \> 部品表およびフォーミュラ \> フォーミュラ** の順に移動します。
1. 関連するフォーミュラを選択します。
1. アクション ウィンドウで、**フォーミュラ** タブの **管理** グループで、**フォーミュラの承認** を選択します。
1. **BOM またはフォーミュラの承認** ダイアログ ボックスで、承認者を選択してから、**OK** を選択します。

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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712913"
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

---
title: 新しいロット ID を選択するとバッチ番号がクリアされる
description: ピッキング リスト仕訳帳の行を確認するときに、[ロット ID] フィールドで新しい値を選択すると、[バッチ番号] フィールドの値がクリアされます。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026662"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>新しいロット ID を選択するとバッチ番号がクリアされる

KB 番号: 4613107

## <a name="symptoms"></a>現象

ピッキング リスト仕訳帳の行を確認するときに、**ロット ID** フィールドで新しい値を選択すると、**バッチ番号** フィールドの値がクリアされます。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。 ロット ID を変更する場合は、品目コンテキストを変更します。 したがって、バッチ番号がリセットされます。

バッチ番号をロット ID に関連付ける場合は、最初にロット ID を設定する必要があります。

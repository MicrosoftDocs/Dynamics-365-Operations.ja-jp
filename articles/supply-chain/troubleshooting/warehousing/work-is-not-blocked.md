---
title: 作業はブロックされていない
description: 作業はブロックされていない
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924207"
---
# <a name="work-isnt-blocked"></a>作業はブロックされていない

エラー コード: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>現象

システムは次のエラー メッセージを表示します。

> ID %1 の作業はブロックされていません。

## <a name="cause"></a>原因

ウェーブの **ブロックされたウェーブ** オプションは、*いいえ* に設定されています。 現在ブロックされていないので、作業のブロックを解除できません。

## <a name="resolution"></a>解像度

 **ブロックされたウェーブ** オプションが *はい* に設定されている場合のみ、ブロックを解除できます。

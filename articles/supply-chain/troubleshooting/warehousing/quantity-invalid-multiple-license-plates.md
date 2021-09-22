---
title: 複数の LP を使用するピッキング作業で数量は無効
description: 複数のライセンス プレートを使用するピッキング作業が 1 つの場所にある場合、ea 単位の数量は無効です。 次のフィールドが正しいことを確認します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476835"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>1 つの場所に複数の LP を使用するピッキング作業がある場合、数量は無効

## <a name="symptoms"></a>現象

複数のライセンス プレートを使用するピッキング作業が 1 つの場所にある場合、*ea* 単位の数量は無効で、次のエラー メッセージが表示されます。

> 数量は単位 1% に対して無効です。

## <a name="resolution"></a>解決策

リリース済み製品または製品バリアントの **単位順序グループ ID** フィールドと **単位換算** フィールドが正しく設定されていることを確認します。

バージョン 10.0.15 では、予定数量を表示するようにエラー メッセージが改善されたことに注意してください ([KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531) を参照)。 新しいエラー メッセージは次のとおりです。

> 数量が無効です。 期待値: %1 %2 です。

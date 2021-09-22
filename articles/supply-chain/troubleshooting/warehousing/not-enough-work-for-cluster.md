---
title: プロファイルの構成後にクラスターのための十分な作業が見つかりません
description: クラスター プロファイルを構成する場合、十分な作業が見つからないというエラー メッセージが表示される場合があります。 プロファイルを編集し、職位を有効化をいいえに設定します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476842"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>システム主導のクラスター ピッキングを使用するときにクラスターのための十分な作業が見つかりません

## <a name="symptoms"></a>現象

*システム主導のクラスター ピッキング* プロセスを使用するとき、(たとえば 10 個の職位がピッキング可能である) クラスター プロファイルを構成している場合は、10 個の職位にピッキングするために十分な作業があればそのプロセスは計画どおりに機能します。 ただし、ピッキングする職位が 8 個しかない場合、次のエラー メッセージが表示されます。

> クラスターのための十分な作業が見つかりません。

## <a name="resolution"></a>解決策

この問題を修正するには、クラスター プロファイルを編集し、**職位のアクティブ化** オプションを *いいえ* に設定します。

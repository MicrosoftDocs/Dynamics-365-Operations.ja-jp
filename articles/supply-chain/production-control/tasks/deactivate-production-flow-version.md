---
title: 生産フロー バージョンの無効化
description: 有効な生産フロー バージョンが不要になった場合、無効化することができます。
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1691dc644e2e191a9e74980784d6dcf741dcd598
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576763"
---
# <a name="deactivate-a-production-flow-version"></a>生産フロー バージョンの無効化

[!include [banner](../../includes/banner.md)]

有効な生産フロー バージョンが不要になった場合、無効化することができます。 すべてのかんばんルールと活動が終了し、今後有効化しない場合にのみ、このオプションを使用する必要があります。 この生産フロー バージョンに関連付けられたすべてのかんばんルールの有効期限は現在の日時に更新されることに注意してください。 

有効な生産フロー バージョンを変更するには、有効なバージョンの有効期限を設定することを検討し、新しいバージョンを作成します。 これにより、新しいバージョンおよび関連するかんばんルールを作成している間、生産の工程を続けることができます。 

有効な生産フロー バージョンを期限切れにするには、有効期限を設定する必要があります。 その意味で、無効化は、ルールというより、例外というようなものです。 

この手順では、無効化することができるバージョンの生産フローが必要です。 バージョンが完全に廃止されていることを 100% 確信しない限り、運用環境にはこれを試みません。


## <a name="deactivate-a-production-flow-version"></a>生産フロー バージョンの無効化
1. [生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. 一覧で、目的のレコードを見つけ、選択します。
5. [無効化] をクリックします。
    * この生産フロー バージョンが廃止であると 100% 確信していない限り次の手順に進まないでください。 [OK] をクリックすると、すべての有効なかんばんルールの期限が切れ、この生産フロー バージョンにおけるすべての生産と補充の活動に即時停止が設定されます。  
6. [OK] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
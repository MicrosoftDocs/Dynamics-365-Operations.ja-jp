---
title: かんばん状態の更新
description: かんばんが誤って空けられるか、または受取済みのかんばんが空けられる必要のある場合、かんばんのステータスを更新する必要があります。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a0e03da4671ffec4ecf4835b20a00ef87971c94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831820"
---
# <a name="update-kanban-status"></a>かんばん状態の更新

[!include [banner](../../includes/banner.md)]

かんばんが誤って空けられるか、または受取済みのかんばんが空けられる必要のある場合、かんばんのステータスを更新する必要があります。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、現場監督を対象としています。


## <a name="find-the-kanban"></a>かんばんを検索します。
1. [生産管理] > [かんばん] > [かんばん] の順に移動します。
2. [材料取り扱い単位] ステータス列のフィルターを開きます。
3. [クリア] をクリックします。
    * これは、フィルターをリセットします。  
4. クイック フィルターを使用して、レコードを見つけます。 たとえば、「000149」という値で [カード番号] フィールドをフィルター処理します。

## <a name="change-emptied-status-to-received-status"></a>空のステータスを受入済ステータスに変更します。
1. 空の材料取り扱い単位の [取り消し] をクリックします。
2. [OK] をクリックします。
    * [材料取り扱い単位] ステータスが受け取られたことに注意してください。  

## <a name="change-received-status-to-emptied-status"></a>受入済ステータスを空のステータスに変更します。
1. 空のかんばんをクリックします。
2. 一覧で、選択された行をマークします。
    * [材料取り扱い単位] ステータスが空になっていることに注意してください。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
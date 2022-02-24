---
title: 輸送管理モードと方法
description: このトピックでは、運輸管理のモードと方法を設定する方法について説明します。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: ceb3930cdb7764f846e88edfff6906b902a7f5fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432428"
---
# <a name="transportation-management-modes-and-methods"></a>輸送管理モードと方法

[!include [banner](../includes/banner.md)]

輸送管理は、積荷未満 (LTL)、トラック積荷 (TL)、または小包などの、配送業者が積荷の配達に使用する輸送のタイプを表します。 輸送方法は、空輸、陸上輸送、船便、鉄道輸送などの、配送業者が積荷の配達に使用する配送形態を表します。

モードと輸送方法は、いくつかの場面で使用されます。 工順計画ではモードのみが使用されますが、出荷配送業者と配送業者サービスを設定する際には、モードと配送方法の両方が使用されます。 モードと輸送方法では、明示的な関係や階層が存在しません。

## <a name="create-a-mode"></a>モードの作成

モードを作成するには、次の手順を実行します。

1. **輸送管理 \> 設定 \> 配送業者 \> 方式** に移動します。
1. **新規作成** を選択して、新しいモードを作成します。
1. モードのための固有 ID および説明のついた名前を入力します。
1. ページを閉じます。

## <a name="create-a-transportation-method"></a>輸送方法の作成

輸送方法を作成するには、次の手順に従います。

1. **輸送管理 \> 設定 \> 配送業者 \> 輸送方法** に移動します。
1. **新規** を選択して新しい配送方法を作成します。
1. 配送方法のための固有 ID および説明のついた名前を入力します。
1. ページを閉じます。

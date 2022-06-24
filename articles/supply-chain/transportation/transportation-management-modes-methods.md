---
title: 輸送管理モードと方法
description: この記事では、運輸管理のモードと方法を設定する方法について説明します。
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1daed8940e41af0163b90195eed64464c2dcac0b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900741"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
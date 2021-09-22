---
title: BOM 展開の動作は、製造オーダーの固定と見積に対して異なります
description: 部品表の展開は、確定した製造オーダーと、手動で作成された作業の見積製造オーダーの間で動作が異なります
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476873"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>BOM 展開の動作は、製造オーダーの固定と見積に対して異なります

## <a name="symptoms"></a>現象

製造オーダーを確定すると、部品表 (BOM) を展開しても品目が展開されません。 ただし、手動で作業指示を作成してから製造オーダーを見積すると、品目が展開されます。

### <a name="resolution"></a>解決策

製造オーダーが確定されたときに発生する展開は計画オーダーを指していますが、この場合、計画オーダーが現在確定されていることを示しているわけではありません。 ただし、製造オーダーが見積済みの場合は、計画オーダーが存在しないリリース済製造オーダーから展開が開始されます。

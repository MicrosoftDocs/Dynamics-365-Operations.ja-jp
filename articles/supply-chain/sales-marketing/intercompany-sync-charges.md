---
title: 会社間諸費用の同期
description: このトピックでは、会社間諸費用の同期について説明します
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4854b698c8046fc603454c4d9d7059c938c70b3
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548381"
---
# <a name="synchronize-intercompany-charges"></a>会社間諸費用の同期

[!include [banner](../../includes/banner.md)]

諸費用は、会社間販売注文書と会社間発注書でのみ同期化され、常に同期されます。

会社間発注書または会社間販売注文書で **価格編集を許可** フィールドが選択されている場合、会社間販売注文書または会社間発注書に手動で諸費用を追加できます。 それ以外の場合はできません。

会社間販売注文書で **価格編集を許可** フィールドが選択されていない場合、会社間販売注文書に手動で諸費用を追加することはできません。

会社間発注書で **価格編集を許可** フィールドが選択されていない場合、会社間発注書に諸費用を追加することはできません。

会社間発注書と会社間販売注文書の両方に対して **価格編集を許可** フィールドが有効化されている場合、両方の注文に諸費用を手動で追加することができます。 ただし、これにより多数の諸費用が誤って追加される可能性があります。

このような競合を回避するためには、諸費用を会社間販売注文書または会社間発注書のいずれか (両方ではなく) に追加できるようにすることをお勧めします。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

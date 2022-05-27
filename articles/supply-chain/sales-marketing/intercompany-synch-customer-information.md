---
title: 会社間顧客情報の同期
description: このトピックでは、会社間注文に対する顧客情報の同期について説明します
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 1949cb69f22ade6b0e03a02c93ad78e8b7e550ae
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672811"
---
# <a name="synchronize-intercompany-customer-information"></a>会社間顧客情報の同期

[!include [banner](../../includes/banner.md)]

顧客情報は、販売注文の作成時、または顧客、仕入先参照、あるいは顧客要求番号の変更時に、**顧客情報** フィールドが有効になっている場合に同期されます。

これらの同期フィールドの値はいつでも変更できます。 ただし、この値が他の会社間注文にコピーされるかどうかは、このパラメーターを選択することでのみ決定できます。 会社間販売注文書の **顧客情報** フィールドを有効にしている場合、会社間販売注文書に対する変更は、会社間発注書に同期されます。 会社間発注書の **顧客情報** フィールドも有効にしている場合は、元の販売注文書にも同期されます。

> [!NOTE]
> 会社間発注書と会社間販売注文書の両方で **顧客情報** フィールドを有効にしている場合、ある会社のある担当者が行った更新は、別会社の別の担当者が行った同じ注文に対する更新によって取り消されます。

会社間発注書の **顧客情報** フィールドを有効にすることをお勧めします。 これにより、元の販売注文書と会社間発注書との間の同期、および会社間発注書から会社間販売注文書への同期が有効になります。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: BOM バージョンの展開
description: この記事では、部品表 (BOM) のバージョンの展開を含むマスター プランのシナリオを説明します。
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55b94bca10441a3757715e02b23f11b2f11650939b6fdcbbf978f896b414d016
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729486"
---
# <a name="explosion-of-a-bom-version"></a>BOM バージョンの展開

[!include [banner](../includes/banner.md)]

この記事では、部品表 (BOM) のバージョンの展開を含むマスター プランのシナリオを説明します。

BOM バージョンの需要展開は、特定サイト (および場合によっては特定倉庫) における各 BOM 明細行品目に対する需要を作ります。 サイト固有 BOM では、各 BOM 明細行に対して、特定の倉庫が定義される可能性があります。 また、各 BOM 明細行に対し、倉庫が必要かどうかが品目の分析コード設定によって決まります。 その後、結果としての各 BOM 明細行品目に対する需要は、追加の需要展開の開始点となります。 このマスター計画シナリオの前提条件を次に示します。

-   サイト分析コードが必須であり、需要トランザクションで入力する必要がある。
-   サイト分析コードが一貫している。 したがって、下位レベル需要のサイトは、初期需要トランザクションのサイトと同じである。

次の図は、マスタ プラン需要展開のプロセス方法を示しています。 ![BOM バージョンを使用した展開が必要。](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>追加リソース

[BOM バージョンの決定](master-plan-bom-version-determined.md)

[マスター プランとマルチサイト機能の概要](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
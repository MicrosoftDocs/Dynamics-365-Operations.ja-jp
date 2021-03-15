---
title: BOM バージョンの展開
description: この記事では、部品表 (BOM) のバージョンの展開を含むマスター プランのシナリオを説明します。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1f50d9f2f7249ecb4090983e245d4700020e0886
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005180"
---
# <a name="explosion-of-a-bom-version"></a>BOM バージョンの展開

[!include [banner](../includes/banner.md)]

この記事では、部品表 (BOM) のバージョンの展開を含むマスター プランのシナリオを説明します。

BOM バージョンの需要展開は、特定サイト (および場合によっては特定倉庫) における各 BOM 明細行品目に対する需要を作ります。 サイト固有 BOM では、各 BOM 明細行に対して、特定の倉庫が定義される可能性があります。 また、各 BOM 明細行に対し、倉庫が必要かどうかが品目の分析コード設定によって決まります。 その後、結果としての各 BOM 明細行品目に対する需要は、追加の需要展開の開始点となります。 このマスター計画シナリオの前提条件を次に示します。

-   サイト分析コードが必須であり、需要トランザクションで入力する必要がある。
-   サイト分析コードが一貫している。 したがって、下位レベル需要のサイトは、初期需要トランザクションのサイトと同じである。

次の図は、マスタ プラン需要展開のプロセス方法を示しています。 ![BOM バージョンを使用した展開が必要    ](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>追加リソース
--------

[BOM バージョンの決定](master-plan-bom-version-determined.md)

[マスター プランとマルチサイト機能の概要](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
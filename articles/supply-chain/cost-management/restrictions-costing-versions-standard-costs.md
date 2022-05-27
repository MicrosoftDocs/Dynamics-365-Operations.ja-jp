---
title: 標準原価の原価計算バージョンの制限
description: このトピックでは、標準原価の原価計算バージョンに適用する制限について説明します。
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11bf14b2926fd4ff053697bef8b7dad781948a2c
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672209"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>標準原価の原価計算バージョンの制限

[!include [banner](../includes/banner.md)]

このトピックでは、標準原価の原価計算バージョンに適用する制限について説明します。 

次の制限は、標準原価原則への保証の順守に役立ちます。

-  品目の原価には、費用が含まれる必要があります。 製造品目の費用は、部品表 (BOM) および工順情報内の償却済固定費を表します。 したがって、これらの費用を単位原価に含める必要があります。 購買品目の費用も品目の単位原価に含まれます。

-  製造品目の標準原価の計算は、標準原価の原価バージョン内の原価レコードに基づく必要があります。 原価データの代わりのソースは、購入品目の購入価格売買契約などのように、予定原価の原価バージョンのみで使用できます。 原価データの代わりのソースは、BOM 計算グループによって定義されます。

-  BOM の計算は、単一レベル展開モードで実行する必要があります。

標準原価の品目原価データは、標準原価または予定原価を含む別の原価バージョンにコピーできます。 ただし、このトピックで先に示した制限は予定原価には適用されないので、予定原価に対する品目原価データは、標準原価を含む原価バージョンにはコピーできません。

## <a name="related-topics"></a>関連トピック

[原価計算バージョンの概要](costing-versions.md)

[非製造環境での標準原価の更新](update-standard-costs-non-manufacturing-environment.md)

[製造品目の標準原価を管理するための準備](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
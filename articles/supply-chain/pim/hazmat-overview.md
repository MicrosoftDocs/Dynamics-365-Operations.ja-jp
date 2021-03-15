---
title: 危険物の概要
description: このトピックでは、製品情報管理と倉庫管理の際における危険物の処理および文書化に関連する機能の概要を示します。
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: ff285e7e8bcdd2a3197f0ccae569ac880b796028
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007594"
---
# <a name="hazardous-materials-overview"></a>危険物の概要

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

送料と配送の規制を維持するには、危険商品として分類された材料を出荷する組織には、その出荷を伴う追加の書類を含める必要があります。 危険物機能により、顧客はリリースされた品目に関する情報を保存することができます。 この情報は、船積書類を準備するために使用できます。 危険な商品を出荷する組織には、出荷プロセスを管理するための独自のプロセスと手順が必要です。 Microsoft Dynamics 365 Supply Chain Managementは、必要なドキュメントの生成を支援するためのツールでしかありません。

次の図は、危険物機能を設定および使用するために必要な手順を示しています。

![危険物機能の設定および使用](media/hazmat-overview.png "危険物機能の設定および使用")

危険物の機能は、製品情報管理で設定されており、倉庫管理を使用して印刷できるドキュメントが用意されています。 したがって、このような領域は、次の 2 つの主要領域で、この機能の確認、設定、および使用を行います。

- **製品情報管理** - リリース済製品に適用できるコードを設定します。
- **倉庫管理** - 出荷用に印刷される追加の出荷ドキュメントと機能します。

> [!IMPORTANT]
> Supply Chain Management の危険物機能には、危険な製品に関連する情報の記録と参照に役立つ、有用な製品情報フィールドと関連機能のコレクションが用意されています。 これらの機能は、出荷する危険物に関する同じ情報を含む出荷ドキュメントの設計と印刷にも役立ちます。 ただし、システムがお客様の国または地域で適用されるすべての規制に自動的に準拠することはありません。 これらのツールは、一般的な規制への準拠を支援することを目的としていますが、それだけでは十分ではなく、そうであることを保証するものでもありません。 組織は、適用されるすべての規制を把握し、それらを遵守するために必要なすべての措置を講じる責任があります。

## <a name="product-information-management"></a>製品情報管理

製品情報管理には、陸路、航空、および海上貨物の様々な危険物リストで提供される参照情報を入力できる一連の設定テーブルがあります。

この機能が開発された場合、次のような一般的な規制が参照されています。

- **ADR** – 陸路による危険物の国際輸送に関連する規制
- **CFR 49** – 危険物の輸送に関する米国の規制
- **IMDG** – 国際海上危険物規則 (IMDG) コード
- **IATA** – 国際航空運送協会 (IATA) 危険物規制

各規制には、危険な商品および参照コードが標準化されています。 従って、Supply Chain Management には、これらのリストの共有コードの参照テーブルが用意されています。 また、各リストには、定義可能な一意のコードもいくつか含まれています。

危険物の規則や値を設定する方法と、その値を適切な製品に割り当てる方法の詳細については、次のトピックを参照してください。

- [危険物の設定](hazmat-setup.md)
- [製品、注文、出荷、積荷の危険物](hazmat-items.md)

## <a name="warehouse-management"></a>倉庫管理

倉庫管理で出荷を準備すると、製品情報管理で設定した情報を使用するいくつかの新しいレポートを印刷できるようになります。 利用可能なレポートとその使用方法の詳細については、[危険物の照会およびレポート](hazmat-reports.md) を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 危険物
description: このトピックでは、環境に保存されている危険物ドキュメントおよび情報に関する情報を提供します。
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: d27ec5b65cc607c22d97c1dc44bb573bc2772611
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243180"
---
# <a name="hazardous-materials"></a>危険物

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

危険物に関する情報は、製品情報管理で設定されています。 このモジュールでは、倉庫管理を使用して印刷できるドキュメントも提供します。

危険物として分類される材料を出荷する場合は、その出荷に対して追加の書類を含める必要があります。 危険物の機能により、顧客は分類情報を保存し、それをリリース品目に関連付けることができます。 この情報は、船積書類を準備するために使用できます。

> [!IMPORTANT]
> Microsoft Dynamics 365 Supply Chain Management の危険物機能には、危険な製品に関連する情報の記録と参照に役立つ、有用な製品情報フィールドと関連機能のコレクションが用意されています。 これらの機能は、出荷する危険物に関する同じ情報を含む出荷ドキュメントの設計と印刷にも役立ちます。 ただし、システムがお客様の国または地域で適用されるすべての規制に自動的に準拠することはありません。 これらのツールは、一般的な規制への準拠を支援することを目的としていますが、それだけでは十分ではなく、そうであることを保証するものでもありません。 組織は、適用されるすべての規制を把握し、それらを遵守するために必要なすべての措置を講じる責任があります。

この機能を使用する前に、次の設定が必要です。

- **製品情報管理:** リリース済製品に適用できるコードを設定します。
- **倉庫管理:** 出荷情報を印刷するには、追加の出荷ドキュメントを使用します。

## <a name="product-information-management"></a>製品情報管理

製品情報管理には、陸路、航空、および海上貨物の危険物リストで提供される参照情報を追加できる一連の設定テーブルがあります。

よく参照される規制の一部を次に示します。

- **ADR** – 陸路による危険物の国際輸送に関連する規制
- **CFR 49** – 危険物の輸送に関する米国の規制
- **IMDG** – 国際海上危険物規則 (IMDG) コード
- **IATA** – 国際航空運送協会 (IATA) 危険物規制

これらの各規制には、参照コードを含む危険物の一覧があります。 輸送の各タイプのリストは、共有国際分類で結合されます。 Supply Chain Management には、これらのリストの共有コードの参照テーブルが用意されています。 また、各リストには、定義可能な一意のコードもいくつか含まれています。

この情報の構成を開始するには、初期パラメーターを構成するために使用できる規制を作成します。

## <a name="warehouse-management"></a>倉庫管理

出荷の準備ができると、いくつかの新しいレポートを印刷できます。 これらのレポートでは、製品情報管理で設定した情報が使用されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 会社間計画
description: このトピックでは、会社間計画について説明し、Microsoft Dynamics 365 Supply Chain Management で計画の最適化を使用して会社間計画を構成する方法を説明します。
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0958ebccba345aa13a95f1fdf03946546cbbb714
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983597"
---
# <a name="intercompany-planning"></a>会社間計画

[!include [banner](../../includes/banner.md)]

組織によっては、物流工程が組織内の他の法人 (会社) に依存している場合もあります。 各法人が個別の勘定科目表を所有するため、これらの工程は会社間の販売と購買を使用して処理されます。

このトピックでは、会社間計画について説明し、Microsoft Dynamics 365 Supply Chain Management で計画の最適化を使用して会社間計画を構成する方法を説明します。

このトピックでは、次の重要な会社間用語を使用します。

- **上流** – 会社またはサプライ チェーンの相対的な参照。 原材料サプライヤーの方向から流れるデータの動きを示します。
- **下流** – 会社またはサプライ チェーンの相対的な参照。 顧客の方向から流れるデータの動きを示します。
- **計画企業内需要** – 下流会社からの製品の計画需要に基づいた、会社の製品に対する計画需要。

マスター プランでは、会社の計画には、別の会社の計画からの計画オーダーに関連する計画企業内需要を含めることができます。 この機能を使用すると、複数の会社間で計画オーダーの完全な透明性が実現するので便利です。 また、必要なすべての計画供給オーダーが作成されますが、会社間需要に対して計画オーダーを確定する必要がありません。

計画されたダウンストリームの需要を含むマスター プランからマスター プランを実行する場合は、関連する会社間仕入先からの計画発注書が需要として計画に含まれます。

## <a name="required-setup"></a>必要な設定

会社間計画を使用するには、次のようにシステムを準備する必要があります。

1. 関連する製品は、関連するすべての会社でリリースする必要があります。 詳細については、Microsoft Learn で [Dynamics 365 Supply Chain Management で会社間取引を構成および使用する](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) を参照してください。
1. 上流会社や関連する既定の在庫分析コード (サイトと倉庫) との会社間リレーションがある仕入先の購買で、ダウンストリームの需要をカバーする必要があります。 詳細については、Microsoft Learn で [Dynamics 365 Supply Chain Management で会社間取引を構成および使用する](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) を参照してください。
1. 上流会社のマスター プランには、計画された下流需要を含める必要があります。また、関連する会社とマスター プランを下流計画で指定する必要があります。

## <a name="include-planned-downstream-demand"></a>下流の計画需要を含める

計画された下流需要が計画に含まれるようにマスター プランを構成するには、次の手順に従います。

1. **マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。
1. マスター プランを選択または作成します。
1. **会社間計画** クイック タブで、次のフィールドを設定します。

    - **計画された下流需要を含める** – このオプションを *はい* に設定して、マスター プランの会社間計画を有効にします。
    - **下流計画** – **計画された下流需要を含める** オプションを *はい* に設定すると、ツール バーとグリッドを使用して、他の会社から要求されたマスター プランを追加できます。

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>複数レベルのペギングを使用して、複数の会社をペギングする

複数レベルのペギングでは、会社間のペギングを表示してサプライがカバーした需要元を確認できます。

複数レベルのペギング情報を表示するには、次の手順を実行します。

1. **マスター プラン \> マスタープラン \> 計画オーダー** の順に移動します。
1. 計画オーダーを、選択するか、表示します。
1. アクション ペインの **表示** タブ、**要件** グループで、**複数レベルのぺギング** を選択します。

### <a name="intercompany-example-that-involves-two-companies"></a>2 つの会社が関わる会社間の例

この例では、USMF 会社で計画製造オーダーを作成し、DEMF 会社で販売注文をカバーします。 USMF では、直接需要は計画企業内需要です。 この需要を USMF で表示するには、マスター プランをまず DEMF で実行してから USMF で実行します。

次の図は、計画製造オーダーの **複数レベルのペギング** ページで、この例がどのように表示されるかを示します。

![2 つの会社が関わる会社間の例](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>3 つの会社が関わる会社間の例

この例では、USMF 会社で計画発注書を作成し、DEMF 会社で販売注文をカバーします。 DEMF および USMF 会社では、直接需要は計画企業内需要です。 この需要を USMF で表示するには、マスター プランをまず FRRT で実行してから DEMF で実行し、最後に USMF で実行します。

次の図は、計画製造オーダーの **複数レベルのペギング** ページで、この例がどのように表示されるかを示します。

![3 つの会社が関わる会社間の例](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
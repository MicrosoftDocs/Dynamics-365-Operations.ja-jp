---
title: コマース階層
description: この記事は、Dynamics 365 Commerce の階層について説明します。
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ae0e2d068d40b61bd1bd258eac3a0e4b5f399e6a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791974"
---
# <a name="commerce-hierarchies"></a>コマース階層

[!include [banner](includes/banner.md)]

この記事は、Dynamics 365 Commerce の階層について説明します。

カテゴリ階層を作成して、チャンネルを使用して販売する製品を整理することができます。 製品階層を使用して、製品を分類またはグループ化できます。 その後、これらの製品を使用して、製品の品揃えと顧客ロイヤルティ プログラムを作成できます。 また、製品の属性またはプロパティの割り当て、価格決定構造の割り当て、製品プロモーションへの製品の挿入、およびレポートでの製品の使用を行うこともできます。 1 つのカテゴリ階層を作成して組織のすべての製品およびカテゴリを表し、複数の目的にそのカテゴリ階層を使用することができます。 また、製品のプロモーションなどの特殊な目的に複数のカテゴリ階層を作成できます。 製品階層を作成する際に、カテゴリ階層の目的を識別するためにカテゴリ階層タイプを割り当てる必要があります。 たとえば、**コマースのナビゲーション階層** タイプが割り当てられている製品階層のみが、製品をカテゴリごとにオンラインで、または販売時点管理 (POS) で表示する場合に参照されます。

## <a name="hierarchy-types"></a>階層タイプ

次の表に、使用できるカテゴリ階層のタイプと各タイプの一般的な目的を示します。

| カテゴリ階層タイプ       | 目的 |
|-------------------------------|---------|
| 製品階層      | 組織の全体的な製品階層を定義するには、この階層タイプを使用します。 販売促進、価格決定とプロモーション、および品揃え計画にこの階層タイプを使用できます。 1 つの階層にのみこの製品グループ タイプを割り当てることができます。 |
| 補助階層 | 作成する追加のカテゴリ階層の場合には、このタイプを使用します。 たとえば、春に水着のプロモーションがあります。 したがって、別のカテゴリ階層に水着製品を追加し、さまざまな製品カテゴリにプロモーション用の価格決定を適用します。 |
| ナビゲーション階層   | この階層タイプを使用すると、製品をグループ化してカテゴリに整理し、製品がオンラインまたは POS で閲覧できるようになります。 |

カテゴリ階層を使用して製品を構造化することで、製品の属性およびプロパティをカテゴリ レベルで設定および管理できます。 これらの属性およびプロパティには、製品分析コードおよび POS の設定が含まれます。 そのカテゴリに割り当てる製品は、定義するプロパティと属性を自動的に継承します。 また、選択したカテゴリの複数の製品に、製品のプロパティ設定を同時にコピーできます。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
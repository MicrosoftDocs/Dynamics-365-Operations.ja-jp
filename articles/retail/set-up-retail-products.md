---
title: 小売製品の設定
description: この記事では、Microsoft Dynamics 365 for Retail での小売製品の設定方法について説明します。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 991546424a95463315eaa73c2776d0defe66def5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546265"
---
# <a name="set-up-retail-products"></a>小売製品の設定

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 for Retail での小売製品の設定方法について説明します。

小売チャネルで製品を再販するには、Dynamics 365 for Retail で製品の作成とコンフィギュレーションを行う必要があります。 小売は、Dynamics 365 for Retail の製品の機能を使用して、製品マスターで組織全体の製品を作成します。 製品の作成、製品のプロパティおよび属性の定義、および小売カテゴリ階層への製品の割り当てを行うことができます。 製品を小売チャンネルで利用可能にして有効な品揃えに追加するには、製品を利用可能にする法人に製品をリリースする必要があります。 小売チャンネルを使用して販売する製品を設定するには、次の作業を行います。

1. 小売製品階層を定義します。 Dynamics 365 for Retail のカテゴリ階層機能を使用することで、小売カテゴリ階層を定義し、小売チャンネルに配分する製品をグループ化および分類できます。 ユーザー定義属性とシステム属性をカテゴリ レベルで定義できます。 その後、カテゴリに割り当てられているすべての製品は、これらの属性を継承します。 複数のカテゴリ階層を定義したり、各製品を複数の階層に割り当てたりすることができます。 ただし、1 つの階層では、各製品を 1 つのカテゴリにのみ割り当てることができます。
2. 製品および製品バリアントを製品マスター追加します。 製品マスターに追加される製品は、製品の全体的な一覧を表します。 製品を 1 つずつ手動で追加したり、仕入先から製品データをインポートしたりすることができます。
3. 法人への製品のリリース 法人にリリースされている製品のみを小売チャンネルで利用可能にすることができます。 初めて製品を定義する場合、製品を組織全体のレベルで定義します。 次に、製品をリリースする 1 つ以上の法人を選択できます。 その後、製品が組織全体の複数の小売チャンネルで利用可能になります。 この機能を使用して、1 回製品を作成し、1 つの場所で製品の属性およびプロパティを更新し、製品が使用可能な小売チャンネルに組織全体の製品を配分できます。
4. 製品を品揃えに追加します。 品揃えは、小売チャンネルで提供する製品の集まりを表します。 1 つまたは複数の品揃えを定義し、各製品を 1 つまたは複数の品揃えに割り当てることができます。 製品を小売チャンネルに割り当てるには、品揃えをそれらの小売チャンネルに割り当てます。 品揃えを作成すると、法人にまだにリリースされていない製品を追加できます。 ただし、製品を小売チャンネルで利用可能にする前に、それらの製品を法人にリリースする必要があります。
5. ナビゲーション階層に製品を追加します。 製品がオンラインまたは販売時点管理 (POS) で閲覧できるようにするためには、[小売ナビゲーション階層] に分類する必要があります。
6. 製品をカタログに追加します。 このステップは POS では省略可能ですが、オンライン ストアでは製品が少なくとも 1 つのカタログに含まれている必要があります。

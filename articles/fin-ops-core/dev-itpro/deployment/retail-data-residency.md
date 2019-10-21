---
title: Retail データの所在地
description: このトピックでは Retail Cloud Scale Unit を配置するときのデータ所在地に関する考慮事項を説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 570c60cdd9e0e9a1b56a94ff516799d831247127
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183382"
---
# <a name="retail-data-residency"></a>Retail データ所在地

[!include[banner](../includes/banner.md)]


## <a name="choose-a-region"></a>地域を選択

Retail Cloud Scale Unit (RCSU) を初期化するときは、ホストするデータ センターの場所を選択する必要があります。 ネットワークの待機時間を最小限に抑えてパフォーマンスを向上するには、RCSU を使用してサービスを提供する予定の小売チャネルに最も近いデータ センターの場所を選択する必要があります。 各データ センターのおおよその場所を参照するには [Azure のリージョン](https://azure.microsoft.com/global-infrastructure/regions/) を参照してください。 [Azure 速度の参照](https://azurespeedtest.azurewebsites.net/) などの Web ベースのユーティリティを参照して、各店舗の場所から Azure データ センターへの待機時間を測定することもできます。 これは RCSU を初期化するときデータ センターを正しく選択することに役立ちます。

## <a name="data-between-regions"></a>地域間のデータ

本社とは異なる場所のデータ センターで RCSU を初期化すると、データはこれらのデータ センター間を定期的に同期して移動します。 システムは特定の種類のデータを転送するようにコンフィギュレーション済みです。 このコンフィギュレーションを変更して異なるデータを同期できます。

データ同期コンフィギュレーションを表示するには **小売** \> **本社の設定** \> **小売用スケジューラ** \> **スケジューラ ジョブ** に移動してデータ同期ジョブとサブジョブを表示します。 同期中のフィールドを表示するには、サブジョブをクリックします。 

## <a name="synchronize-specific-segments-of-records"></a>レコードの特定の区分を同期する

Commerce Data Exchange (CDX) を構成して、レコードの特定の区分のみを特定の RCSU に同期することができます。 

### <a name="prerequisites"></a>必要条件

同期するレコード区分を構成する前に、チャネル データベース グループを構成する必要があります。 これらのデータベース グループは、セグメント化されたデータを同期する各 RCSU に対して構成する必要があります。 同じチャネル データベース グループ内のすべての RCSU は、その RCSU 内のすべてのチャネルにサービスを提供するのに必要なデータを受け取ります。 セグメント化されたデータを同期させる予定の各 RCSU チャネル データベースに対して、別々のデータベース グループを作成する必要があります。 それには、次の手順を実行します:

1. **小売** \> **本社の設定** \> **小売用スケジューラ** \> **チャンネル データベース グループ**の順に移動します。
2. セグメント化されたデータを同期させる各 RCSU に対して新しいデータベース グループを作成します。
3. **小売** \> **本社の設定** \> **小売用スケジューラ** \> **チャンネル データベース** の順に移動します。
4. 対応する Retail Cloud Scale Unit のチャネル データベースを選択します。
5. **編集** を選択し、ステップ 2 で作成したチャネル データベース グループを選択します。
6. **保存** を選択します。 
7. 選択したチャンネル データベースに対して **すべてのジョブの完全データ同期** を選択します。

### <a name="available-controls-for-synchronizing-segments-of-data-to-different-rcsus"></a>データの区分を異なる RCSU に同期させるための利用可能なコントロール

チャンネル コンフィギュレーション データは、特定の RCSU によって提供されるチャンネルに対してのみ同期されます。 たとえば、西ヨーロッパのチャンネルで配信されるように構成された小売チャンネルのチャンネル コンフィギュレーション データのみがその RCSU に同期されます。 

品揃えを使用して、商品および価格設定に関連するデータを特定のチャネルでセグメント化できます。 たとえば、北米の店舗が婦人靴のみを販売し、西ヨーロッパの店舗がスポーツ用品のみを販売する場合は、品揃えを使用してこのデータをセグメント化できます。 データが RCSU に同期されている場合、婦人靴のデータは北米の RCSU にのみ同期され、スポーツ用品のデータは西ヨーロッパの RCSU にのみ同期されます。

顧客レコードと従業員レコードはグローバル アドレス帳を使用して構成し、それは特定の小売チャネルに対して構成できます。 たとえば、西ヨーロッパの RCSU と北米の RCSU で提供されるチャネル用に、顧客と従業員用に別々のアドレス帳を構成できます。

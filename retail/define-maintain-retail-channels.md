---
title: "小売チャンネルの定義と管理"
description: "この記事では、Microsoft Dynamics 365 for Retail では小売店舗とも呼ばれる、従来型の店舗を設定するプロセスの概要を説明します。 ここでは、小売店舗を設定する前と後の、実施する必要のあるタスクについて説明します。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 3f0b566963574569cb40b72550e2337c9ba8a2ce
ms.contentlocale: ja-jp
ms.lasthandoff: 06/20/2017


---

# <a name="define-and-maintain-retail-channels"></a>小売チャンネルの定義と管理

[!include[banner](includes/banner.md)]


この記事では、Microsoft Dynamics 365 for Retail では小売店舗とも呼ばれる、従来型の店舗を設定するプロセスの概要を説明します。 ここでは、小売店舗を設定する前と後の、実施する必要のあるタスクについて説明します。

Dynamics 365 for Retail は、オンライン ストア、コール センター、また実店舗などの、複数の小売チャンネルをサポートします。 従来型の店舗は、小売店舗とも呼ばれます。 各小売店舗は、独自の支払方法、価格グループ、POS レジスタ、収入/経費勘定、およびスタッフを持つことができます。 作成する前に、小売店舗のこれらすべての要素を設定する必要があります。 小売店舗を作成したら、店舗に配送される製品を割り当てます。 また、店舗への従業員、レジスター、および顧客の割り当ても行います。 最後に、組織階層に新しい店舗を追加します。

## <a name="setting-up-retail-stores"></a>小売店舗の設定
Dynamics 365 for Retail で小売店舗を設定する前に、必要なタスクを完了する必要があります。 その後、小売店舗を作成し、詳細を追加できます。

### <a name="prerequisites"></a>必要条件

小売店舗を設定する前に次の作業を行う必要があります。

1.  組織構造を設定し、小売品揃え、補充、およびレポートの組織階層を設定します。
2.  小売店舗を表す倉庫を設定します。
3.  小売店舗、店舗明細書と明細書の伝票の番号順序を設定します。
4.  小売用パラメーターをコンフィギュレーションします。
5.  店舗で受け入れる支払方法を設定します。
6.  Retail POS のレジスターでクレジット カード取引を処理する場合、支払サービスも設定できます。
7.  売上税グループを設定します。
8.  小売製品を設定します。 このタスクの一部として、小売製品階層、製品バリアントおよび製品の品揃えを設定します。
9.  製品価格グループを設定します。
10. 小売製品価格を設定します。 このタスクの一部として、価格調整、割引および割引期間を設定します。
11. スタッフ メンバーを設定します。 **メモ:** Dynamics 365 for Retail for Retail POS システムを使用してサインインし、タスクを実行できるように、作業者に適切なアクセス許可を割り当てる必要があります。
12. 店舗に割り当てる Retail POS のプロファイルをコンフィギュレーションします。 タスクには、登録設定、オフライン プロファイルの設定、レシートの形式とプロファイルの設定などの多くのタスクが含まれます。

これらの前提条件に含まれるタスクすべてを確認し、適用するタスクのみを実行します。

### <a name="set-up-a-retail-store"></a>小売店舗の設定

必要な作業を完了した後、小売店舗の詳細を設定する次のタスクを実行します。

1.  小売店舗を作成します。
2.  店舗に売上税グループを割り当てます。
3.  店舗に受け入れられている支払方法を割り当てます。
4.  小売店舗で提供する製品の説明に詳細を追加します。 たとえば、リッチ テキストと画像を追加できます。 これらの製品の詳細は POS レジスターやまたは印刷されたラベルなど、さまざまなコンテキストに表示されます。
5.  **小売品揃え**、**小売補充**、または**小売レポート**のために割当てられる既存の組織階層に店舗を追加します。

### <a name="after-you-set-up-a-retail-store"></a>小売店舗を設定した後

小売店舗の詳細を入力したら、Retail POS に新しい小売店舗のデータを送信するための次のタスクを実行します。

1.  店舗の POS レジスターをコンフィギュレーションします。
2.  店舗に、製品の品揃えを割り当てます。
3.  品揃えを処理し、品揃えに含める製品のリストを生成して製品を小売店舗で販売できるようにします。
4.  番号順序、ハードウェア プロファイル、POS 画面レイアウトなどのデータを Retail POS レジスターに送信します。
5.  小売店舗を公開して、Retail POS に店舗データを送信します。
6.  Retail POS に店舗のデータを送信するジョブを実行します。

## <a name="organization-hierarchies"></a>組織階層
Retail は、組織階層を使用して小売チャンネルを構成します。 組織階層は、業務を構成する組織の関係を表します。 店舗を設定すると、組織階層にその店舗を追加することができます。 店舗では、品揃え、補充、およびレポートに使用されるデータを共有します。





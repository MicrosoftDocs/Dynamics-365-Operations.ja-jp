---
title: 在庫エイジング レポート ストレージ
description: このトピックでは、在庫エイジング レポートを実行し、その出力をフォームおよびグラフとして使用できるようにする機能について説明します。
author: AndersGirke
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ddddb0b1e377ed525b7c17fec5a4b3305573d0eba551bc03f075109a2ed769b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781113"
---
# <a name="inventory-aging-report-storage"></a>在庫エイジング レポート ストレージ

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management では、**在庫のエイジング レポート ストレージ** を実行して、フォームとグラフとして出力できるようにします。 フォームでは、コンフィギュレーションされているレイアウトに応じて、列と集計残高が動的に調整されます。 チャートは、フィルター処理をサポートする視覚概要を提供します。詳細にドリルダウンすることができます。 さらに、**在庫エイジング レポート** という名前のデータ エンティティを使用すると、実行された **在庫エイジング レポート ストレージ** レポートの結果を Microsoft Excel ファイルや PDF ファイルなどの形式でエクスポートできます。

**在庫エイジング レポート ストレージ** レポートを実行するこの方法は、出力に多数の行が含まれている場合に便利です。 たとえば、倉庫として作成された 50,000 個の品目と 300 軒の店舗がある場合、出力には多くの明細行が含まれ、在庫エイジングは、品目、サイト、および倉庫ごとに要求します。

## <a name="enable-the-inventory-value-storage-report-feature"></a>在庫評価額ストレージ レポート機能を有効にします

この機能を使用するには、事前にシステム上で有効にする必要があります。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して機能状態を確認し、必要に応じてそれを有効にすることができます。 この機能は次のように一覧表示されます。

- **モジュール** - 原価管理
- **機能名称** - 在庫エイジング レポート ストレージ

## <a name="run-an-inventory-aging-report-storage"></a>在庫評価額レポート ストレージを実行する

1. **原価管理 \> 照会およびレポート \> 在庫エイジング レポート ストレージ** の順に移動します。
1. **新規** を選択します。
1. **プロセス ID – 名前** フィールドに、レポートの固有の名前を入力します。
1. **ID – ID** レポートを選択し、必要に応じてフィルター処理します。

    レポートの実行は、常にバッチ ジョブで行われます。

1. バッチ ジョブが完了すると、出力は **在庫エイジング レポート ストレージ** ページに表示されます。
1. 従来のグリッド レイアウトを持つフォームとして出力を表示するには、**詳細の表示** を選択します。 集計グラフとして出力を表示するには、**グラフの表示** を選択します。

    > [!NOTE]
    > フォームには、レポート レイアウトで定義されている小計は含まれません。

**在庫エイジング レポート** データ エンティティを使用すると、**プロセス ID – 名前** フィールドのフィルターを、データ管理がサポートする形式に適用することにより、**在庫エイジング レポート ストレージ** レポートをエクスポートできます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
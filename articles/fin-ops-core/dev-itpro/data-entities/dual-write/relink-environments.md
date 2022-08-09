---
title: 二重書き込み環境のリンク解除および再リンク
description: この記事では、リンクの解除、キー テーブルのクリア、および二重書き込み環境の再リンクの方法について説明します。
author: RamaKrishnamoorthy
ms.date: 04/07/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: ''
ms.openlocfilehash: e313f20c87c6ba62d74cdd36e1c0990deafaa68c
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111410"
---
# <a name="unlink-and-relink-dual-write-environments"></a>二重書き込み環境のリンク解除および再リンク

[!include [banner](../../includes/banner.md)]



環境間の二重書き込み接続のリンクを解除および再リンクする場合は、キー テーブルからデータを削除する必要があります。 この要件は、バックアップや復元などの活動中の、サンドボックス、運用、およびユーザー承認テスト (UAT) 環境に適用されます。 この記事では、リンクの解除、キー テーブル内のデータの削除、二重書き込み環境の再リンクの方法について説明します。

マッピングは Dataverse に格納されるので、リンクを解除および再リンクした場合マッピングは保存されます。

## <a name="scenario-dual-write-is-enabled-between-production-environments"></a>シナリオ: 運用環境間で二重書き込みを有効にする

このシナリオでは、財務と運用と Dataverse 運用環境の間で二重書き込みを有効にします。 財務と運用運用環境 (ソース) をバックアップし、それを財務と運用 UAT 環境 (出力先) に復元するとします。 復元したら、財務と運用 UAT 環境で次の手順に従ってください:

1. すべてのテーブル マップを停止します。
2. 財務と運用 UAT 環境が Dataverse 運用環境を指すように、二重書き込み接続を解除します。
3. キー テーブルからデータを削除します。

    - **DualWriteProjectConfiguration**
    - **DualWriteProjectFieldConfiguration**
    - **BusinessEventsDefinition**

4. 財務と運用 UAT 環境に対して、Dataverse UAT 環境を再リンクすることが必要な場合があります。 
5. マッピングを有効にします。

Dataverse でバックアップおよび復元のプロセスが実行されている場合は、次の手順に従います。

1. 財務と運用 UAT 環境にサインインします。
2. すべてのテーブル マップを停止します。
3. Dataverse UAT 環境が、財務と運用の運用環境を指すように、二重書き込み接続を解除します。
4. Dataverse の **二重書き込みランタイムのコンフィギュレーション** テーブルからデータを削除します。
5. 財務と運用 UAT 環境に対して、Dataverse UAT 環境を再リンクすることが必要な場合があります。
6. マッピングを有効にします。

## <a name="scenario-reset-or-change-linking"></a>シナリオ: リンクのリセットまたは変更

二重書き込みに関連付けられている既存のサンドボックス Dataverse インスタンスをリセットする場合、または別の Dataverse インスタンスにリンクを変更する場合は、次の手順に従います。

1. 財務と運用アプリにサインインします。
2. すべてのエンティティ マップを停止します。
3. 財務と運用アプリと Dataverse の間の二重書き込み接続のリンクを解除します。
5. Dataverse 環境をリセットします。
6. 財務と運用アプリでキー テーブルからデータを削除します。

    - **DualWriteProjectConfiguration**
    - **DualWriteProjectFieldConfiguration**
    - **BusinessEventsDefinition**

7. リセットする環境に二重書き込みを設定します。 詳細については、[システム要求と前提条件](requirements-and-prerequisites.md) を参照してください。

## <a name="known-issues"></a>既知の問題

### <a name="secureconfig-organization-error"></a>SecureConfig の組織エラー

環境をコピーした後にレコードをコピー、更新、または削除しようとする場合、**SecureConfig Organization (ProjVcTest4) が実際の CRM 組織 (org6459f7a8_195867911_20200717T174709) と一致しない** というエラーが発生します。

エラーを軽減するには、次の手順に従います。

1. Customer Engagement アプリで、**高度な検索** を選択します。
2. **検索** フィールドで、**二重書き込みランタイムのコンフィギュレーション** を選択します。
3. **結果** を選択します。
4. 行が表示されます。 すべての行を選択します。
5. **削除** アイコンを選択します。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


---
title: Invoice Capture ソリューションのダッシュボード
description: この記事では、Invoice Capture ソリューションのダッシュボードについて説明します。
author: sunfzam
ms.date: 10/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690123"
---
# <a name="invoice-capture-solution-dashboard"></a>Invoice Capture ソリューションのダッシュボード

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Invoice capture では、ダッシュボードにインポートされた請求書の概要を示すグラフが表示されます。 これらのグラフは、買掛金勘定 (AP) マネージャによる請求書生成プロセスのパフォーマンスを分析する際に役立ちます。 AP マネージャは、請求書作成プロセスの状態を確認できるほか、さまざまなフィルターを適用して詳細を確認することもできます。

## <a name="available-charts"></a>使用可能なグラフ

以下のグラフは、ダッシュボードで利用できます:

- **状態別にキャプチャされたすべての請求書**: このグラフには、キャプチャされた請求書の次のステータスが表示されます。 状態を選択することで、ユーザーは、詳細な一覧でキャプチャされた請求書をフィルターできます。

    - キャプチャ
    - 完了
    - レビュー中
    - 廃止

- **キャプチャされた請求量の合計** - このグラフは、期間別にキャプチャされた請求書の数を示します。 ユーザーは、ドロップダウン リストを使用して期間を変更できます。
- **上位ベンダーからキャプチャされた請求量** - このグラフは、ベンダーごとの請求書の総数を示しています。 請求書が最も多いベンダーが上部に表示されます。
- **例外を含む請求書ごとの完了日数** - このグラフは、1 件の請求書を取り込むのに必要な平均日数を示します。 この情報は、手動での確認が必要な場合に、AP マネージャが請求書の処理時間を分析する場合に役立ちます。 増加傾向にある場合、ユーザーはプロセスの詳細を確認し、設定を調整することで、所要日数の短縮に役立てることができます。
- **保留時間による請求書の不備** - このグラフは、ERP (Enterprise Resource Planning) システムにおいて、取り込まれた請求書が作成されていない日数を示しています。 保留日数が多いほど、請求書作成プロセスが長くなります。 AP マネージャーは、取り込んだ詳細な請求書をドリルダウンし、ERP システムで請求書を作成することができます。

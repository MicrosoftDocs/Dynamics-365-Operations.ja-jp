---
title: キャッシュ フロー予測における外部データ
description: このトピックでは、外部データを入力したり、キャッシュフロー予測にインポートしたりするために実行する必要がある設定ステップについて説明します。
author: rcarlson
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66b097b2936e61c619d45ad103440eddbb983feb
ms.sourcegitcommit: c8dc60bb760553f166409c2e06dd2377f601c006
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/23/2021
ms.locfileid: "7945794"
---
# <a name="external-data-in-cash-flow-forecasts"></a>キャッシュ フロー予測における外部データ

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

外部データを入力したり、キャッシュフロー予測にインポートしたりできます。 このトピックでは、外部データの使用に固有であり、外部データをキャッシュ フロー予測に含められるようにするための設定ステップについて説明します。

## <a name="external-data-setup"></a>外部データの設定

**キャッシュフロー予測設定** ページ (**キャッシュおよび銀行の管理 \> キャッシュ フロー予測 \> キャッシュ フロー予測の設定**) の **外部ソース** タブを使用して、キャッシュフロー予測での外部データの使用をサポートする設定を入力します。

外部データを入力したり、キャッシュフロー予測にインポートしたりできます。 外部データの入力またはインポートを行う前に、外部ソースを設定する必要があります。 **外部ソース** タブで、外部キャッシュ フロー カテゴリを設定します。 カテゴリは、**発信** または **着信** のいずれかです。 転記タイプとして **流動性** を選択する必要があります。 **法人設定** グリッドで、外部キャッシュ フロー カテゴリが適用される法人および対応する主勘定を選択します。

キャッシュ フロー予測の設定方法の詳細については、[キャッシュ フロー予測](../cash-bank-management/cash-flow-forecasting.md)を参照してください。

## <a name="enter-external-data"></a>外部データの入力

キャッシュフロー予測の外部データを入力および変更するには、**Excelで開く** の機能を使用できます。 **キャッシュ フロー予測設定** ページの **外部データ** ボタンを選択し、**外部データの追加** または **既存の外部データの編集** を選択します。 Microsoft Excel ファイルを開くと、次のフィールドに情報を入力できます。

- **入力 ID** (一意)
- **説明** (オプション)
- **外部ソース名** - Finance Insights 情報の設定時に定義した一覧の値のいずれかを選択します。
- **法人**
- **日**
- **トランザクション通貨の金額**
- **通貨コード**
- **既定の分析コード** (オプション)
- **ドキュメント番号** (オプション)
- **口座番号** (オプション)
- **口座名** (オプション)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>データ管理フレームワークを使用した外部データのインポート

キャッシュフロー予測の外部データは、**データ管理** ワークスペースと、**キャッシュ フロー予測の外部ソース エントリ** と呼ばれるエンティティを使用してインポートできます。

また、設定データをある環境から別の環境に移動する必要がある場合は、必要な設定テーブルに対して次のエンティティ領域が用意されています。

- キャッシュ フロー予測の外部ソースの設定
- キャッシュ フロー予測の外部ソース法人の設定

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: キャッシュ フロー予測に外部データを使用する (プレビュー)
description: このトピックでは、外部データを入力したり、キャッシュフロー予測にインポートしたりするために実行する必要がある設定ステップについて説明します。
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 801327dc54f6d4cfef7a9f062395e29846783e8f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644948"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>キャッシュ フロー予測に外部データを使用する (プレビュー)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

外部データを入力したり、キャッシュフロー予測にインポートしたりできます。 このトピックでは、外部データの使用に固有であり、外部データをキャッシュ フロー予測に含められるようにするための設定ステップについて説明します。

## <a name="external-data-setup"></a>外部データの設定

**キャッシュフロー予測設定** ページ (**キャッシュおよび銀行の管理 \> キャッシュ フロー予測**) の **外部ソース** タブを使用して、キャッシュフロー予測での外部データの使用をサポートする設定を入力します。

設定の詳細については、[キャッシュ フロー予測](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting) を参照してください。

キャッシュフロー予測の外部データを入力するには、[Excelで開く] の機能を使用して、外部データを入力および変更します。 **外部データ** ボタンを選択し、**外部データの追加** または **既存の外部データの編集** を選択します。 Microsoft Excel ファイルを開くと、次のフィールドに情報を入力できます。

- **入力 ID**
- **説明** (オプション)
- **外部ソース名** - Finance 分析情報の設定時に定義した一覧の値のいずれかを選択します。
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

#### <a name="privacy-notice"></a>プライバシー通知
プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。
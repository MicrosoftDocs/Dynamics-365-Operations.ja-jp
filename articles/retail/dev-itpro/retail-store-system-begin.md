---
title: Retail Store Scale Unit
description: このトピックでは、Retail Store Scale Unit とそれを使用する場合について説明します。
author: athinesh99
manager: AnnBe
ms.date: 12/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail
ms.custom: 219714
ms.assetid: 773fb32d-14c1-4dc8-8330-0332c6a037a2
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fe22915375f31ce8273b744685057dac2aff621c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368896"
---
# <a name="retail-store-scale-unit"></a>Retail Store Scale Unit

[!include [banner](../includes/banner.md)]

このトピックでは、Retail Store Scale Unit とそれを使用する場合について説明します。

<a name="overview"></a>概要
--------

Retail Store Scale Unit は、バック オフィスまたは本社 (HQ) への常時インターネット接続がない店舗で製品の販売をサポートする一連の機能です。 Store Scale Unit は、店舗内の工程専用に設計されており、インターネット サービスが貧弱な場合でもターミナル間トランザクションおよびシフト操作が可能になります。 バック オフィスに自動的に接続することで、インターネット接続がある場合に、店舗はクレジット カード トランザクションを処理し、ギフト カードを発行し、HQ シームレスにデータを同期させることができます。 Store スケール ユニットは、標準 HQ 配置でダウンロードできます。

## <a name="is-the-retail-store-scale-unit-right-for-you"></a>Retail Store Scale Unit は自分に適切ですか。
Store スケール ユニットのセットアップを開始する前に、このオプションが店舗に好適かどうかを多少の時間をとって判断してください。 Store Scale Unit は、インターネット接続が低速または切断されやすい店舗を持っており、各店舗のオンプレミスに Store Scale Unit を展開する柔軟性を必要としている小売業者が選択できる展開です。 安定したインターネット接続があり、クラウド環境の待ち時間が小さいシナリオでは、Store Scale Unit をセットアップせずに店舗をクラウドとしてのみ運用することを考慮することをお勧めします。 始める前に、次の点を考慮してください。

-   Store Scale Unit またはクラウド専用システムとしての店舗を設定する営業案件は 1 件だけです。 Store スケール ユニット有効の店舗からクラウド専用の店舗への移動は、既定ではサポートされず、手動での構成が必要になります。
-   Store Scale Unit では、店舗内の MPOS および Cloud POS の両方がサポートされます。
-   Store Scale Unit は、1 台のコンピューター上の 1 ボックス配置トポロジでセットアップするか (推奨)、異なるコンピューター上の複数ボックス トポロジでセットアップできます。
-   ボックス環境の店舗スケール単位オプションを選択した場合、設定の多くは事前に設定されます。 マルチボックス トポロジに関しては、手動でコンポーネント間の接続をコンフィギュレーションする必要があります。
-   Store スケール ユニットで、ユーザーはトランザクションの中断/取り消しおよびシフト操作と同様に、複数の POS デバイスでクロス ターミナル シナリオを実行できます。
-   Store Scale Unit では、本社または支払プロバイダーへのインターネット接続がない限り、ユーザーはギフト カードの発行、製品の検索、クレジット カード トランザクションの実行などのリアルタイム操作を実行することはできません。 取引の大部分でリアルタイムのトランザクションが関係する場合、Store Scale Unit が、HQ または支払プロバイダーへの接続を有効にするには、インターネットに常に接続されている必要があります。
-   店舗スケール ユニットでは、POS からチャネル データベースへの直接データベース接続はサポートされていません。 Store スケール ユニットの POS デバイスは、常に操作の実行に Retail Server を使用します。

> [!NOTE]
> Retail Store Scale Unit はオフラインでは置き換えられないことに注意してください。 現時点では、オフライン データベースを持つ Retail Modern POS でのみオフライン機能を使用できます。 

## <a name="get-started-with-store-scale-unit"></a>Store Scale Unit の使用を開始する

開始するには、店舗規模単位の構成に関する [Retail Store Scale Unit の設定およびインストール](retail-store-scale-unit-configuration-installation.md) トピックを確認してください。

<a name="additional-resources"></a>追加リソース
--------

[Retail Store Scale Unit ダウンロードおよびセルフ サービスでの構成](retail-store-scale-unit-configuration-installation.md)




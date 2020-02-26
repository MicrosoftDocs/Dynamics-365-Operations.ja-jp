---
title: コマース スケール ユニット
description: このトピックでは、Commerce Scale Unit と、どんなときにそれを使用するかについて説明します。
author: athinesh99
manager: AnnBe
ms.date: 12/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 219714
ms.assetid: 773fb32d-14c1-4dc8-8330-0332c6a037a2
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 08b8e734a5481fc0071fc3c0e390e56a862c8e93
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004627"
---
# <a name="commerce-scale-unit"></a>コマース スケール ユニット

[!include [banner](../includes/banner.md)]

このトピックでは、Commerce Scale Unit と、どんなときにそれを使用するかについて説明します。

<a name="overview"></a>概要
--------

Commerce Scale Unit は、バック オフィスまたは本社 (HQ) への常時インターネット接続がない店舗で製品の販売をサポートする一連の機能です。 Store Scale Unit は、店舗内の工程専用に設計されており、インターネット サービスが貧弱な場合でもターミナル間トランザクションおよびシフト操作が可能になります。 バック オフィスに自動的に接続することで、インターネット接続がある場合に、店舗はクレジット カード トランザクションを処理し、ギフト カードを発行し、HQ シームレスにデータを同期させることができます。 Store スケール ユニットは、標準 HQ 配置でダウンロードできます。

## <a name="is-the-commerce-scale-unit-right-for-you"></a>Commerce Scale Unit は自分に適切ですか。
Commerce Scale Unit のセットアップを開始する前に、このオプションが店舗に好適かどうかを多少の時間をとって判断してください。 Commerce Scale Unit は、インターネット接続が低速または切断されやすい店舗を持っており、各店舗のオンプレミスに Commerce Scale Unit を展開する柔軟性を必要としている小売業者が選択できる展開です。 安定したインターネット接続があり、クラウド環境の待ち時間が小さいシナリオでは、Commerce Scale Unit をセットアップせずに店舗をクラウドとしてのみ運用することを考慮することをお勧めします。 始める前に、次の点を考慮してください。

-   Store Scale Unit またはクラウド専用システムとしての店舗を設定する営業案件は 1 件だけです。 Commerce Scale Unit が有効の店舗からクラウド専用の店舗への移動は、既定ではサポートされず、手動での構成が必要になります。
-   Commerce Scale Unit では、店舗内の MPOS およびクラウド POS の両方がサポートされます。
-   Commerce Scale Unit は、1 台のコンピューター上の 1 ボックス配置トポロジでセットアップするか (推奨)、異なるコンピューター上の複数ボックス トポロジでセットアップできます。
-   ボックス環境のオプションを選択した場合、設定の多くは事前に設定されます。 マルチボックス トポロジに関しては、手動でコンポーネント間の接続をコンフィギュレーションする必要があります。
-   Commerce Scale Unit で、ユーザーはトランザクションの中断/取り消しおよびシフト操作と同様に、複数の POS デバイスでクロス ターミナル シナリオを実行できます。
-   Commerce Scale Unit では、本社または支払プロバイダーへのインターネット接続がない限り、ユーザーはギフト カードの発行、製品の検索、クレジット カード トランザクションの実行などのリアルタイム操作を実行することはできません。 トランザクションの大部分でリアルタイムのトランザクションが関係する場合、 HQ または支払プロバイダーへの接続を有効にするには、インターネットに常に接続されている必要があります。
-   Commerce Scale Unit では、POS からチャネル データベースへのダイレクト データベース接続はサポートされていません。 POS デバイスは、操作の実行に常に Commerce Scale Unit を使用します。

> [!NOTE]
> Commerce Scale Unit はオフラインでは置き換えられないことに注意してください。 現時点では、オフライン データベースを持つ Retail Modern POS でのみオフライン機能を使用できます。 

## <a name="get-started-with-store-scale-unit"></a>Store Scale Unit の使用を開始する

開始するには、次の Commerce Scale Unit の構成に関するトピック、[Retail Store Scale Unit の構成とインストール](retail-store-scale-unit-configuration-installation.md) を確認してください。

<a name="additional-resources"></a>追加リソース
--------

[コンフィギュレーションおよびインストール Retail Store Scale Unit](retail-store-scale-unit-configuration-installation.md)




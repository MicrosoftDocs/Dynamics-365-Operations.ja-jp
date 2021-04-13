---
title: POS のクライアント イメージ
description: このトピックは、小売環境で POS クライアント イメージ管理に関連する機能を実装するユーザーを対象としています。 実装の計画時に考慮すべき実装のヒントとガイダンスについて説明します。
author: josaw1
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: cbittner
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: b9d241752b5e25e6c6612a8a8e49ef6cd32700e0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804345"
---
# <a name="client-images-in-pos"></a>POS のクライアント イメージ

[!include [banner](includes/banner.md)]

このトピックは、小売環境で POS (販売時点管理) クライアント イメージ管理に関連する機能を実装するユーザーを対象としています。 実装の計画時に考慮すべきヒントとガイダンスについて説明します。

このガイドは、クラウド POSと Modern POS の両方に適用されます。これにより、ストアでのユーザー エクスペリエンスを強化し、アップセル、クロスセル、顧客サービスなどの顧客中心のシナリオをサポートするために使用できるイメージ ファイル サイズの処理とイメージのタイプに関する一般情報が提供されます。 ようこそ画面イメージ、カテゴリ イメージ、および製品イメージは、使用できるイメージ タイプの一例です。

## <a name="implementation-considerations"></a>実装の考慮事項

- **ファイル サイズ** - さまざまなタイプのイメージをロードしながら、POS クライアント ユーザー インターフェイス (UI) とパフォーマンスの応答性を維持するために、使用目的に応じて適切なファイル サイズになるようにイメージを準備することをお勧めします。 たとえば、Contoso デモ データ内の製品およびカテゴリのイメージのサイズは、500 x 500 または 580 x 580 ピクセルです。

- **イメージ サイズ** - POS デバイスの画面とディスプレイは、適正なイメージ サイズ (長さと幅) を事前に決定します。 イメージ サイズは、意図した画面サイズにできるだけ近づける必要があります。 例については、以下の「実装の例」セクションを参照してください。

- **解決策** - 考慮すべき重要なパラメーターは、1 インチあたりのドット数 (dpi)、または画面解像度の場合は 1 インチあたりのピクセル数 (ppi) です。 POS クライアント イメージは印刷されないため、Web 上で画像を表示するための共通 dpi 設定は適切なガイドラインです (72 ~ 150 dpi)。 Contoso デモ イメージ ファイルは、通常 96 dpiで表示されます。 高解像度のデバイスの場合、実際のピクセルではなく、オペレーティング システム (OS) のスケーリングを考慮し、有効な解像度を使用する必要があります。

- **ファイル タイプ** –  \*.png または \*.jpg イメージ ファイル タイプを使用できます。 ほとんどの場合、\*.jpg のサイズは小さくなります。

## <a name="implementation-example"></a>実装の例 
1366 x 768 ピクセルの解像度と Contoso デモ データに類似した画面レイアウトを備えた一般的な 18.5 インチ PO Sディスプレイで、キャンバスの 3 分の 2 をカバーするウェルカム画面イメージを作成するには、画面の長さと幅よりもそれほど高くない解像度の画像を選択します。 この例では、911 x 512 ピクセルの解像度で十分です。 長さと幅に比較的高い解像度を選択しても、低い dpi 設定を維持すると、ファイル サイズは適度に小さくなります。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
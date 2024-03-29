---
title: 混合ライセンス プレートの受取
description: この記事では、混合ライセンス プレート受取の登録方法とモバイル デバイスの複数品目の作業方法について説明します。
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76ba316a5ed55902aed35acb4ef21623c7676b38
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907061"
---
# <a name="mixed-license-plate-receiving"></a>混合ライセンス プレートの受取

[!include [banner](../includes/banner.md)]

混合ライセンス プレート受取では、プット アウェイ作業を登録し作成する前に、複数品目で構成されているライセンス プレートを構築することができます。 

複数品目で構成されるライセンス プレートは、各品目を登録するための入荷ドックで分割する必要はありません。 

元伝票の明細行を識別するために、フローに関連する品目を使用する場合は、品目コントロール上のバーコードをスキャンすることができます。 バーコードに数量とコンフィギュレーションされた測定単位 (UOM) がある場合は、品目および数量が自動的に混在ライセンス プレートに追加され、もう 1 つの品目をスキャンする画面に戻ります。 これにより、ステップごとに確認することなく、素早くすべての品目をスキャンすることができます。 

混合ライセンス プレートの受取フローでは、ライセンス プレートに既にスキャンされた品目の一覧を表示し、ここから正しい品目の数量に修正することができます。

## <a name="where-it-applies"></a>該当する場所

混合ライセンス プレート受取とは、同時に複数明細行 / 品目の作業を登録し作成するモバイル デバイスの受取フローです。 これは、複数品目を含む入庫ライセンス プレートを受け取る場合に便利です。 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a>混合ライセンス プレートの受取の設定方法
混合ライセンス プレートの受取は、モバイル デバイスのメニュー品目として設定されます。

既存の作業ではなく、次の方法のいずれかを使用するモード作業で、新しいメニュー品目を作成します。

- 混合ライセンス プレートの受取
- 混合ライセンス プレートの受取とプット アウェイ

元伝票の明細行を識別するためのオプションとして、発注書の品目、発注書の明細行、返品注文、移動オーダーの品目、および在庫移動指示明細行があります。 これらのオプションは、1 つのライセンス プレートの入荷注文に変更できます。 最後のオプションは、負荷品目によるものです。 複数の品目をライセンス プレートに追加することはできますが、複数の負荷を切り替えることはできません。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: 予測明細行から倉庫需要予測分析コードを削除できない
description: 予測明細行から倉庫需要予測分析コードを削除できません。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026680"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>予測明細行から倉庫需要予測分析コードを削除できない

KB 番号: 4614408

## <a name="symptoms"></a>現象

この問題は、**需要予測パラメータ** ページの **予測分析コード** タブで **倉庫** 分析コードが割り当てられていない場合に発生します。 しかし、**倉庫** 列は **需要予測** ページ (**マスター プラン \> 予測 \> 手動予測エンティティ \> 需要予測明細行**) に表示されます 。

## <a name="resolution"></a>解像度

**需要予測パラメータ** ページの **予測分析コード** タブの設定は、**需要予測** ページ には影響しません。 予測コードは、調整済み需要予測で生成および表示されるベースライン予測を制御します。 ただし、「実際の」需要予測に必要な分析コードは制御しません。 **調整済需要予測** ページに表示されるレコードを承認することで、予測モデルの「実際の」予測エントリに変換できます。 その後、そのモデルをマスター プランに使用できます。

**需要予測** ページでは、需要予測明細行に表示される「実際の」予測の分析コードが在庫分析コードの一部になります。 (この動作は、販売注文明細行の動作と似ています。) **倉庫** を必須の在庫分析コードとして使用するようシステムを設定していない場合は、ページをカスタマイズして列を非表示にできます。

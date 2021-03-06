---
title: 1 つのレシートの複数の作業ヘッダーに対して印刷されるラベルは 1 つのみである
description: 1 つのレシートの複数の作業ヘッダーに対して印刷されるラベルは 1 つのみです。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026676"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>1 つのレシートの複数の作業ヘッダーに対して印刷されるラベルは 1 つのみである

KB 番号: 4614667

## <a name="symptoms"></a>現象

単一の倉庫アプリ受信イベントの一環で、同じターゲット ライセンス 契約に対して複数の作業ヘッダーが作成されます。 ただし、製品を入庫する際に印刷されるライセンス ラベルは 1 つのみです。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。

現在の設計では、作業ヘッダーと作業ラインに存在する組み合わせの数に関係なく、常に 1 つのライセンス ラベルが生成されます。 生成されたラベルには、1 つの組み合わせについての情報だけが含まれます。

この問題を回避するには、作業ヘッダーの作成が常に 1 つのターゲット ライセンス契約にマッピングされるようにします。

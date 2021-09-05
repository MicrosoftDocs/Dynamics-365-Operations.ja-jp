---
title: インポート ジョブで日時を同期する
description: インポート ジョブで UTC タイム ゾーンを使用して、タイム ゾーンの変換に関する問題を回避します。
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c76eadc5839785ba1624ee3894ef1d0872369aa9
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403844"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>インポート ジョブで日時を同期する

[!include [banner](../includes/banner.md)]

インポート ジョブのタイム ゾーンを協定世界時 (UTC) に設定することが重要です。 別の設定を使用すると、インポート データに予期しない日付と時刻が表示される場合があります。 正しい設定を行わないと、インポート プロセスで UTC の日付がローカル形式に変換され、システム設定で再度変換されます。

この二重変換によって、アプリケーション間で日付が変更されます。 たとえば、二重変換では、ローカル タイム ゾーンの違いにより Dynamics 365 Human Resources と Dynamics 365 Finance の間で従業員の開始日が異なる場合があります。 インポート ジョブを UTC に設定すると、この問題が解決します。

1. Dynamics 365 Finance and Operations で、**データ管理** を選択します。

2. **プロジェクトのインポート** を選択し、プロジェクトを選択します。

3. **ソースの日付形式** で **CSV-Unicode** を選択します。

   [![ソースの日付形式を UTC に変更。](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. **タイム ゾーン** を **協定世界タイムゾーン** に変更し、**言語** を **En-US** に変更します。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

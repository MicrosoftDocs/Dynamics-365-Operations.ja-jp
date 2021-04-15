---
title: インポート ジョブで日時を同期する
description: インポート ジョブで UTC タイム ゾーンを使用して、タイム ゾーンの変換に関する問題を回避します。
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748672"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>インポート ジョブで日時を同期する

[!include [banner](../includes/banner.md)]

インポート ジョブのタイム ゾーンを協定世界時 (UTC) に設定することが重要です。 別の設定を使用すると、インポート データに予期しない日付と時刻が表示される場合があります。 正しい設定を行わないと、インポート プロセスで UTC の日付がローカル形式に変換され、システム設定で再度変換されます。

この二重変換によって、アプリケーション間で日付が変更されます。 たとえば、二重変換では、ローカル タイム ゾーンの違いにより Dynamics 365 Human Resources と Dynamics 365 Finance の間で従業員の開始日が異なる場合があります。 インポート ジョブを UTC に設定すると、この問題が解決します。

1. Dynamics 365 Finance and Operations で、**データ管理** を選択します。

2. **プロジェクトのインポート** を選択し、プロジェクトを選択します。

3. **ソースの日付形式** で **CSV-Unicode** を選択します。

   [![ソースの日付形式を UTC に変更](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. **タイム ゾーン** を **協定世界タイムゾーン** に変更し、**言語** を **En-US** に変更します。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
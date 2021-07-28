---
title: 固定資産の仕損としての処分
description: このトピックでは、仕損として処分された固定資産のトランザクションを除去するプロセスについて説明します。
author: moaamer
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 0e465594968ac860a9cb8f6f5d679084e5594457
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355608"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>固定資産の仕損としての処分

[!include [banner](../includes/banner.md)]

このトピックでは、仕損として処分された固定資産のトランザクションを除去するプロセスについて説明します。 削除できるトランザクションタイプには、資産の取得、減価償却トランザクションなどの固定資産トランザクションが含まれます。 これらのトランザクションが削除されると、取得原価調整、減価償却調整、再評価、評価増および評価減の勘定など、貸借対照表の勘定に影響を与えます。

| 取引                                         | 借方 (Dr.) | 貸方 (Cr.) |
|-----------------------------------------------------|-------------|--------------|
| Dr. 減価償却累計額                        | x           |              |
| Cr. 固定資産の利益/損失                          |             | x            |
| Dr. 固定資産の利益/損失                          | x           |              |
| Cr. 固定資産の取得勘定                 |             | x            |
| Dr. 固定資産の利益/損失 (正味簿価額 \[NBV\]) | x           |              |
| Cr. 固定資産の利益/損失 (NBV)                    |             | x            |

> [!NOTE]
> 会社の最高財務責任者 (CFO) または管理者と密接に協力して、各トランザクション タイプに使用する適切な勘定を識別し、処分プロセスとトランザクションを検証して、アカウントの正しい更新を生成することをお勧めします。

固定資産を仕損として処分する前に、資産の取得金額、今年度の減価償却、前年度の減価償却、および資産の NBV に関連付けられている勘定科目を作成する必要があります。 固定資産トランザクション タイプは、**固定資産転記プロファイル** ページに一覧表示されます。  **固定資産 \> 設定 \> 固定資産転記プロファイル** の順に移動し、**処分** クイック タブでグリッドの上のフィールドにある **仕損** を選択します。 次の図は、**固定資産の転記プロファイル** ページにある固定資産トランザクション タイプの一覧を示しています。


[![仕損としての資産の処分 (図1)。](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

次の例では、2018 年 1 月 1 日に取得された固定資産が 2019 年 3 月 31 日に仕損されます。

- **取得価格:** 24,000.00 米ドル (USD)
- **耐用年数:** 2 年間
- **減価償却方法:** 定額法耐用年数
- **減価償却額:** 毎月 1,000.00 USD

固定資産の NBV は次の式を使用して計算されます。

正味簿価額 = 取得価格 – 減価償却

この例では、固定資産が取得されて、2018 年 1 月から 2019 年 3 月までの 15 か月間の減価償却が行われました。 したがって、資産の NBV は9,000.00 USD (24,000.00 USD – 15,000.00 USD) になります。

[![固定資産の減価償却の例。](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


処分仕訳帳を作成するには、**固定資産 \> 仕訳入力 \> 固定資産仕訳帳l** の順に移動し、アクション ウィンドウで、**明細行** を選択します。 **処分 - 仕損** を選択し、固定資産 ID を選択します。 資産を完全に処分するには、**借方** フィールドまたは **貸方** フィールドに値を入力しないようにします。

[![固定資産仕訳帳。](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

固定資産の処分仕損トランザクションでは、固定資産帳簿のフィールド値が次のように変更されます。

- **残高** セクションで、**ステータス** フィールドが **仕損** に更新されます。
- **払出** セクションで、**処分日** フィールドは資産が仕損された日付に設定されます。

[![固定資産仕訳帳の詳細。](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

次の図は、固定資産の残高を示しています。

[![固定資産の残高。](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

次の図は、転記された伝票を示しています。

[![正味帳簿価格。](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
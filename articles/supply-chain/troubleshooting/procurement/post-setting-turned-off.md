---
title: 元帳設定の勘定への転記の設定が有効になっていない
description: この問題は、"買掛金勘定パラメータ" ページの "請求書" タブで、"元帳の掛売勘定に転記" オプションが有効になっていて発注書が請求されるときに発生します
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476896"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>元帳設定の勘定への転記の設定が有効になっていない

## <a name="symptoms"></a>現象

この問題は、**買掛金勘定パラメータ** ページの **請求書** タブで、**元帳の掛売勘定に転記** オプションを *はい* に設定された時に発注書が請求されるときに発生します。

## <a name="reproduce-the-issue"></a>問題を再現する

この問題を再現する一つの方法は次のプロシージャです。

1. **買掛金勘定 \> 設定 \> 買掛金勘定パラメーター** の順に移動します。
1. **請求書** タブで、**元帳の掛売勘定に転記** オプションを *はい* に設定します。
1. **在庫管理 \> 設定 \> 転記 \> 転記** に移動します。
1. **発注書** タブで、製品の購買経費のすべての明細行が削除されていることを確認します。
1. **買掛金勘定 \> 発注書 \> すべての発注書** に移動します。
1. 発注書を作成します。 **仕入先勘定** フィールドで、*1001 Acme 事務用品* を選択します。
1. 以下の設定で注文書明細行を追加します。

    - **品目番号:** *D0011 レーザー プロジェクター*
    - **サイト:** *1*
    - **倉庫:** *11*
    - **数量:** *4*

1. アクション ペインで、**購入** タブの **アクション** グループで、**確認** を選択します。
1. アクション ペインの、**受領** タブの **一般** グループで、**製品受領書** を選択します。
1. **製品受領書の転記** ダイアログボックスの **製品受領書** フィールドに任意の番号を入力し、**OK** を選択します。
1. アクション ペインの、**請求書** タブで、**生成** グループから **請求書** を選択します。
1. **番号** フィールドに、請求書番号として任意の数を入力します。
1. 照合状態を更新して、転記します。
1. 発注書から請求書を生成すると、"製品タイプの取引タイプに対する仕入先の勘定番号が存在しません。" というエラーが表示されることに注意してください。

## <a name="resolution"></a>解決策

これは、請求書および請求書グループのパラメータ設定によって異なります。 詳細については、[発注書と在庫の変動に関する会計転記](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/) を参照してください。

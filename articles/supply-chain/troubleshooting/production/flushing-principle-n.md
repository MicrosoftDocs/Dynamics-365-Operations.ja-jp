---
title: BOM 明細行の部品消費ルールの設定が念入りではない
description: 部品表 (BOM) 明細行の部品消費ルールの設定が念入りではない。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ee40eff53efd920ebe43a7b2dd28129f01e6ebb5e75bd480a91f758529f77fc5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716959"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a>BOM 明細行の部品消費ルールの設定が念入りではない

KB 番号: 4612725

## <a name="symptoms"></a>現象

この問題は、**生産管理パラメータ** ページの **自動更新** タブの **自動 BOM 消費** フィールドが *部品消費ルール* に設定 されている場合に発生します。 この設定は、発注書を受け取った時点で、すべての部品表 (BOM) 明細行が自動的に消費されます。 BOM 明細行の **部品消費ルール** フィールドが明示的に *手動* に設定されている場合は、BOM 明細行が自動的に消費される可能性が 生じない可能性があります。 ただし、この問題が発生すると、**部品消費ルール** フィールドが *手動* に設定されている BOM 明細行が自動的に消費されます。

## <a name="resolution"></a>解像度

この問題が発生した場合は、BOM 明細行の **部品消費ルール** の設定を上書きするために生産管理パラメータが設定されている可能性があります。 **生産管理パラメータ** ページの **自動更新** タブで、**自動 BOM 消費** フィールドの値を確認 します。 *常時* に設定されている場合、システムは、すべての BOM 明細行の **部品消費ルール** 設定を無視し、常に明細行をフラッシュします。 BOM 明細行の **部品消費ルール** 設定をシステムで適用するには、**自動 BOM 消費** フィールドの値を *部品消費原則* に変更します 。

---
title: eコマース チャネルで一貫した配送モードの処理を有効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce の e コマースチャネルの課金フローに関連する可能性のある問題に対処する、一貫した配送モードの処理を有効にする方法について説明します。
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 4cecd70dacd72572afc8e6cb65530bf2be4cc93d
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349952"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>eコマース チャネルで一貫した配送モードの処理を有効にする 

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の e コマースチャネルの課金フローに関連する可能性のある問題に対処する、一貫した配送モードの処理を有効にする方法について説明します。

Dynamics 365 Commerce では、比例しないヘッダーレベルの課金は、eコマース チャネルでは既定で適用されません。 この動作は、eコマース チャネルにおいて、以下のいずれか、または両方の問題を引き起こす可能性があります。

- プロットされないヘッダー レベルの料金は表示されません。
- 配送方法の選択とチェックアウトの注文概要の間で、配送方法の料金が統一されていません。

これらの問題を解決するためには、**チャネルにおける一貫した配信モードの取り扱いを可能にする** 機能をオンにする必要があります。 この機能により、比例しないヘッダー レベルの料金がeコマースチャネルに表示され、販売注文の配送情報が同じリクエスト ワークフローで一貫して処理されることが保証されます。

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>チャネルでの一貫した配信モードの処理を有効にする機能をオンにする

Commerce 本部で **チャネルにおける一貫した配信モードの取り扱いを可能にする** 機能を有効にするには、次の手順に従います。

1. **機能管理** ワークスペース (**システム管理 \> ワークスペース \> 機能管理**) を開きます。
1. 利用可能な機能の一覧から、**チャネルにおける一貫した配信モードの取り扱いを有効にする** を検索して選択します。
1. 右側のペインで、**今すぐ有効にする** を選択します。

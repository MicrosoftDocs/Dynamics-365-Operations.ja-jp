---
title: eコマース チャネルで一貫した配送モードの処理を有効にする
description: この記事では、Microsoft Dynamics 365 Commerce の e コマース チャネルの課金フローに関連する可能性のある問題に対処する、一貫した配送モードの処理を有効にする方法について説明します。
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: f32f1915f8f7de1d5536b69b05bc74c6149dfda6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885588"
---
# <a name="enable-consistent-delivery-mode-handling-in-e-commerce-channels"></a>eコマース チャネルで一貫した配送モードの処理を有効にする 

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の e コマース チャネルの課金フローに関連する可能性のある問題に対処する、一貫した配送モードの処理を有効にする方法について説明します。

Dynamics 365 Commerce では、比例しないヘッダーレベルの課金は、eコマース チャネルでは既定で適用されません。 この動作は、eコマース チャネルにおいて、以下のいずれか、または両方の問題を引き起こす可能性があります。

- プロットされないヘッダー レベルの料金は表示されません。
- 配送方法の選択とチェックアウトの注文概要の間で、配送方法の料金が統一されていません。

これらの問題を解決するためには、**チャネルにおける一貫した配信モードの取り扱いを可能にする** 機能をオンにする必要があります。 この機能により、比例しないヘッダー レベルの料金がeコマースチャネルに表示され、販売注文の配送情報が同じリクエスト ワークフローで一貫して処理されることが保証されます。

## <a name="turn-on-the-enable-consistent-delivery-mode-handling-in-channel-feature"></a>チャネルでの一貫した配信モードの処理を有効にする機能をオンにする

Commerce 本部で **チャネルにおける一貫した配信モードの取り扱いを可能にする** 機能を有効にするには、次の手順に従います。

1. **機能管理** ワークスペース (**システム管理 \> ワークスペース \> 機能管理**) を開きます。
1. 利用可能な機能の一覧から、**チャネルにおける一貫した配信モードの取り扱いを有効にする** を検索して選択します。
1. 右側のペインで、**今すぐ有効にする** を選択します。

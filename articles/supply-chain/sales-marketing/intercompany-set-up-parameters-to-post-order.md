---
title: 会社間注文を転記するパラメータの設定
description: このトピックでは、会社間注文を転記するためのパラメーターを設定する方法について説明します
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 24389d8ed3768089d59dc87e5948e9ea7fa1ecfc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679250"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>会社間注文を転記するパラメータの設定

[!include [banner](../../includes/banner.md)]

会社間顧客請求書の転記時に、会社間発注書と元の顧客請求書の両方を自動的に転記するように設定できます。

> [!NOTE]
> この手順を実行する前に、適切な請求書プリンターを指定するように組織内の印刷管理を設定します。 これにより、元の販売注文の請求書が適切なプリンターで印刷されるようになります。

次のパラメータを設定する必要があります:

1. **販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。 使用する販売注文を選択します。
1. 販売注文のアクション ペインで **ヘッダーの表示** を選択し、**会社間設定** クイック タブを選択して開きます。
1. **販売注文** タブのアクション ペインに移動し、**編集** を選択します。
1. **会社間設定** クイック タブに戻り、**直納** を選択し、会社間グループ全体 (すべての注文) への直納を有効にします。
1. 新しい設定で販売注文を保存するには、**保存** を選択します。 その後、**閉じる** を選択して販売注文を閉じます。
1. **調達 \> 仕入先 \> すべての仕入先** の順に移動します。 **全般** タブで **会社間** を選択します。
1. **会社間** ページで **発注書ポリシー** リンクを選択します。 **会社間発注書 (直納)** フィールド グループで **請求書の自動転記** を選択し、**請求書の自動印刷** フィールドからチェック マークを外します。
1. **元の販売注文書 (直納)** フィールド グループで、**請求書の自動転記** フィールドと **請求書の自動印刷** フィールドを選択します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

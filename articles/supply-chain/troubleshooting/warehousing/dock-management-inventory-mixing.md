---
title: ドック管理プロファイルを使用する場合の混合在庫タイプ
description: ドック管理プロファイルで在庫の混合を効果的に管理するには、作業ヘッダーの区切りを最初に設定する必要があります。 このページでは、操作方法について説明します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476860"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>ドック管理プロファイルを使用する場合、在庫タイプは混合されている

## <a name="symptoms"></a>現象

*出荷連結ポリシー* を使用しています。 *場所プロファイル* の *ドック管理プロファイル* を設定しましたが、作業の作成時には、最終的な場所で在庫タイプが混合します。

## <a name="resolution"></a>解決策

ドック管理プロファイルでは、事前に作業を分割する必要があります。 つまり、ドック管理プロファイルでは、作業ヘッダーに複数のプット場所がないことを想定しています。

ドック管理プロファイルで在庫の混合を効果的に管理するには、作業ヘッダーの区切りを設定する必要があります。

この例では、ドック管理プロファイルは **混合しない在庫タイプ** を *出荷 ID* に設定されるように構成しています。その場合は、作業ヘッダーの区切りを設定します。

1. **倉庫管理 \> 設定 \> 作業 \> 作業テンプレート** の順に移動します。
1. 編集する **作業指示書のタイプ** (*発注書* など) を選択します。
1. 編集するには、作業テンプレートを選択します。
1. アクション ウィンドウで、**クエリの編集** を選択します。
1. **並べ替え** タブを開き、次の設定で行を追加します。
    - **テーブル** - *一時的な作業トランザクション*
    - **派生テーブル** - *一時的な作業トランザクション*
    - **フィールド** - *出荷 ID*
1. **OK** を選択します。
1. **作業テンプレート** ページに戻ります。 アクション ウィンドウで、**作業ヘッダーの分割** を選択します。
1. アクション ウィンドウで、**編集** を選択します。
1. **フィールド名***出荷 ID* に関連付けられているチェックボックスをオンにします。
1. アクション ウィンドウで、**保存** を選択します。
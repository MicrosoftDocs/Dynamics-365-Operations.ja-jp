---
title: 資産の重要度タイプ
description: この記事では、資産管理の資産の重要度タイプについて説明します。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfde9a9bc681c0d758491fc5c361b5b046e20d9d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899501"
---
# <a name="asset-criticality-types"></a>資産の重要度タイプ

[!include [banner](../../includes/banner.md)]

 

この記事では、資産管理の資産の重要度タイプについて説明します。 資産の重要度は資産に関連し、ワーク オーダーに転送されます。 ワーク オーダーでは変更できません。 資産の重要度は、ワーク オーダー スケジューリング中にワーク オーダーの重要度を計算するために使用されます。 つまり、資産のどのメンテナンス ジョブが会社の生産スケジュールと生産性にどの程度影響するかを計算するために使用されます。 ワーク オーダー スケジューリングの評価スコアの計算に関連する設定の詳細については、[資産管理パラメーター](../setup-for-objects/enterprise-asset-management-parameters.md) を参照してください。

重要度を設定するには、まず資産設定で使用する重要度タイプを作成します。 それから、資産の重要度の設定をします。

## <a name="set-up-criticality-types"></a>重要度タイプの設定

1. **資産管理** \> **設定** \> **資産** \> **重要度タイプ** を選択します。
2. **新規** を選択してレコードを作成します。
3. **重要度** フィールドに、重要度を示す数値を入力します。
4. **名前** フィールドに、重要度タイプの名前を入力します。
5. **係数** フィールドに係数を入力します。 この係数は、ワーク オーダー スケジューリングの計算中に使用され、重要度レコードが使用されるべきかを決定します。 (最も高い係数を持つレコードは常に使用されます。) この設定は、次の図に示すように、同じ重要度値を持つ重要度明細行が作成されている場合に関係します。

    ![重大度タイプ ページ。](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>資産の重要度の設定

1. **資産管理** \> **設定** \> **資産の重要度** を選択します。
2. **新規** を選択してレコードを作成します。
3. 資産の重要度の特定のレベルの詳細に応じて、**機能場所**、**資産タイプ**、**メーカー**、**モデル**、**資産**、**ジョブ タイプ カテゴリ**、**ジョブ タイプ**、**ジョブ タイプ バリアント** および **ジョブ要件** フィールドで関連する選択を行います。

    > [!NOTE]
    > 資産の重要度が選択されると、資産管理はすべての資産重要度レコードを調べて、一致の可能性をチェックします。 常に最も限定的な組み合わせを最初にチェックします。 つまり、資産管理は、まず **ジョブ要件** をチェックします。 一致するものが見つからない場合は、**ジョブ タイプ バリアント** がチェックされます。 一致するものが見つからない場合は、**ジョブ タイプ** などがチェックされます。 ページのレイアウトで分かるように、この動作は、最も限定的な組み合わせを見つけるために、資産管理が各レコードを右から左に一致をチェックすることを意味します。 一致するものが見つからない場合は、選択がない「既定」のレコードが使用されます。

4. **重要度** フィールドで、前の手順で作成した重要度値の一つを選択します。

### <a name="notes-about-criticality-setup"></a>重要度の設定に関する注記

- ワーク オーダーで既に使用した後に、この設定で資産の重要度を変更した場合、ワーク オーダーにある重要度は適宜更新されません。
- ワーク オーダーにある重要度は、ワーク オーダーにワーク オーダー明細行が追加または削除されるたびに再計算されます。
- ワーク オーダーに複数のワーク オーダー ジョブが含まれている場合、**重要度タイプ** ページの **係数** フィールドに従って、ワーク オーダーでは常に最高の重要度が使用されます。
- 一般に、資産の重要度は一定期間で変化する可能性があります。 重要度は、新しい機器の購入、改修などによって影響を受ける可能性があります。 資産の重要度を定期的に再評価し (たとえば、1 年または 1 年おきに 1 回)、重要度の定義が現在の生産の設定と一致していることを確認してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
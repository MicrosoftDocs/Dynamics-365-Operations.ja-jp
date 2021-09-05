---
title: 組み込みマスター計画と計画最適化の違い
description: このトピックでは、計画の最適化がまだサポートしていない機能と、そのプログラムを計画の最適化に合わせて分析ページに示していない機能の一覧を示します。
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a102f1d77362f650c060ce5d0aee5b62d2102532
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344957"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>組み込みマスター計画と計画最適化の違い

[!include [banner](../../includes/banner.md)]

計画の最適化の結果は、組み込みマスター計画エンジンと結果が異なる場合があります。 違いは保留されている機能が原因で引き起こさせる可能性があります。 このトピックでは、計画の最適化がまだサポートしていない機能および **[計画の最適化に合わせた解析](planning-optimization-fit-analysis.md)** ページ] に一覧化されていない機能を表示します。

| フィーチャー | 計画の最適化における現在の動作 |
|---|---|
| CW 製品 | CW 製品は通常の製品と見なされます。|
| 拡張可能な分析コード | 計画オーダーで拡張分析コードは、**分析コードによる補充計画** チェックボックスが **保管分析コード グループ** または **追跡分析コード グループ** ページで、選択されている場合でも空です。 |
| フィルター処理された生産実行 | 詳細については、[生産計画 - フィルター](production-planning.md#filters) を参照してください。 |
| 予測計画 | 予測計画はサポートされていません。 予測モデルをマスター プランに割り当てる場合は、マスター プランを使用することをお勧めします。 |
| 計画されたオーダーの番号シーケンス | 計画されたオーダーに対する番号シーケンスはサポートされていません。 サービス側で計画されたオーダー番号が生成されます。 |
| コピーの計画、計画の削除、および計画バージョン クリーンアップ | <p>次の項目は、ナビゲーション ウィンドウの **マスター計画 \> マスター計画 \> 計画の維持** で無効になっています。</p><ul><li>コピーの計画</li><li>計画の削除</li><li>計画バージョンのクリーンアップ</li></ul> |
| 返品注文 | 返品注文は考慮されません。 |
| 関連機能のスケジューリング | 詳細については、[無限能力を使用したスケジューリング](infinite-capacity-planning.md#limitations) を参照してください。 |
| 配送カレンダー | **出荷のモード** ページで **配送カレンダー** 列の値は無視されます。 |

## <a name="additional-resources"></a>追加リソース

- [計画最適化適合分析](planning-optimization-fit-analysis.md)
- [計画の最適化で使用されないパラメーター](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

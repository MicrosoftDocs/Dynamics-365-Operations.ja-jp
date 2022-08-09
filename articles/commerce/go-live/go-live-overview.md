---
title: Go-Live および更新の推奨事項の概要
description: この記事では、Microsoft Dynamics 365 Commerce 実装プロジェクトの実行や更新に役立つ作業に関する情報を提供します。
author: mssle
ms.date: 07/08/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: sheaton
ms.search.validFrom: 2021-09-20
ms.openlocfilehash: 705955ea66a4c541fc7ece75b2a557749edfbbbd
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129492"
---
# <a name="go-live-and-update-recommendations-overview"></a>Go-Live および更新の推奨事項の概要

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 実装プロジェクトの実行や更新に役立つ作業に関する情報を提供します。 円滑および効果的に機能するように、システムの構成に役立つコンテンツへのリンクを提供します。

> [!NOTE]
> 記事の一覧は、時間の経過とともに拡大します。 リリース時に考慮される可能性があるすべての品目の完全な一覧は表示されません。

始める前に、[現在の移動チェックリスト](https://aka.ms/d365fogolivechecklist) のコピーをダウンロードします。

## <a name="improve-performance"></a>パフォーマンスの改善

移動または更新プロセスを完了している間に、パフォーマンスを向上させることができます。

### <a name="optimize-images"></a>画像の最適化

Web サイトのパフォーマンスは、通常、画像のダウンロードによって影響されます。 画像のサイズを小さくし、Commerce での画像の使用を最適化することで、Web サイトのパフォーマンスを向上させることができます。 詳細については、[画像の最適化](performance-optimize-images.md) を参照してください。

### <a name="reduce-javascript-by-excluding-unused-modules"></a>使用されていないモジュールを除外して JavaScript を削減する

Commerce で使用されていない JavaScript モジュールを除外することで、Web サイトのパフォーマンスを向上させることができます。 詳細については、[未使用のモジュールを除外した JavaScript の削減](performance-reduce-javascript.md) を参照してください。

### <a name="add-or-update-robotstxt"></a>robots.txt の追加または更新

検索リンクによるサイトの予期しない、または方向性のないクロールにより、「404 ページが見つかりません」というエラーが多く引き起こされる場合があります。 これらのエラーは、サイトが存在しない多くのページ要求に応答するときにパフォーマンス上の問題につながる可能性があります。 この問題を解決するには、常に有効な robots.txt ファイルをアップロードして、準拠するクローラーがサイト内の関連するページのみを探すように誘導する必要があります。 詳細については、[robots. txt ファイルの追加または更新](add-robots-txt.md) を参照してください。

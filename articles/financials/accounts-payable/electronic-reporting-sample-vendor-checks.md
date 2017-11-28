---
title: "電子レポートのサンプル仕入先小切手"
description: "このトピックでは、電子レポートのサンプル小切手フォーマットの使い方についての一般情報を提供します。"
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c9abea228cdaae84ca2b9aada9f36bbe79c1dc6b
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a>電子レポートのサンプル小切手フォーマット

電子レポート (ER) を使用して仕入先小切手をフォーマットすることができます。 市場では多くの銀行固有の、および小切手プロバイダー固有の小切手フォーマットが使用可能です。 サンプル小切手フォーマットは、ER ツール リポジトリの支払小切手モデルに含まれています。 これらのサンプル小切手には、「**小切手中央 (米国)**」および「**小切手上控え下 (米国)**」というラベルが付いています。

## <a name="what-check-formats-are-currently-supported"></a>どんな小切手フォーマットが現在サポートされていますか？

Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリに移動して、**GER コンフィギュレーション** という資産タイプを持つ利用可能なファイルの現在のリストを表示する必要があります。 「何を設定する必要がありますか。」という次のセクションに、利用可能なコンフィギュレーションを確認し選択したコンフィギュレーションをインポートできるよう LCS リポジトリを作成する方法を説明するトピックへのリンクが含まれています。

Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition には、上部に小切手がありその後に 2 つの送金セクションがあるサンプル フォーマットが含まれています。 小切手が真ん中、つまり 2 つの送金セクションの間にあるサンプル フォーマットも含まれています。 これらのサンプル形式は、Deluxe 業務用小切手フォーマットに対応します。

## <a name="what-do-i-have-to-set-up"></a>何を設定する必要がありますか。

- ER を使用して小切手を印刷するには、少なくとも 1 つの有効な小切手コンフィギュレーションを ER コンフィギュレーションにインポートしておく必要があります。 手順については、[Lifecycle Services の電子申告コンフィギュレーションのダウンロード](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)を参照してください。
- 銀行口座に現金および銀行管理小切手をコンフィギュレーションする時は、[**一般的な電子エクスポート形式**] チェック ボックスを選択してから、適切な小切手フォーマットをエクスポート形式コンフィギュレーションとして選択します。
- 送金に印刷される伝票の明細行の数を指定する必要もあります。 この数を計算する際は確実にヘッダー行も含めるようにします。 2 つのサンプル小切手フォーマットについては、推奨される明細行の数は 17 です。 ただし、小切手ストックおよびプリンター ドライバーによってこの番号は異なります。
- テスト用小切手を印刷して小切手のレイアウトを検証することをお勧めします。 テスト用小切手を印刷するには、[**印刷テスト**] オプションを選択します。 サンプル小切手フォーマットは、Microsoft Excel の詳細なプリンターのプロパティで [**余白**] を [**なし**] に設定すると最適に機能します。 テスト用小切手が生成されてから、Excel 出力の編集機能を有効にし、すべての余白が **0** (ゼロ) に設定されるようにページ レイアウトを構成します。 小切手のテスト コピーを小切手ストックと比較し、配置に問題がなくなるまで設定を調整します。
- 支払仕訳でコンフィギュレーションしてある銀行口座に対する支払を生成する時、小切手は指定されたフォーマットを使用して印刷されます。

詳細については、「[電子レポートのフォーマットを修正する](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md)」を参照してください。


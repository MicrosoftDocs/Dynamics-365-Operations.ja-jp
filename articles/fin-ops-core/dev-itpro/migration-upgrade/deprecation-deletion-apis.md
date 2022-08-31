---
title: 方法とメタデータの要素の廃止
description: この記事では、コード ベースの拡大に伴って古くなるメソッドよびメタデータ要素の廃止に関する情報が提供されます。
author: gianugo
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 4dab7b440cc5752324f4374bdf0f88626587c36c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279398"
---
# <a name="deprecation-of-methods-and-metadata-elements"></a>方法とメタデータの要素の廃止

[!include[banner](../includes/banner.md)]

Microsoft コード ベースが進歩すると共に、いくつかのメソッドとメタデータ要素が不要になります。 Microsoft は、これらの古いメソッドとメタデータ要素を廃止とマークします。

- メソッドは **SysObsolete** 属性でマークされます。 通常、この属性は、代わりの方法を推奨します。
- メタデータ要素の場合、**IsObsolete** プロパティが **Yes** に設定されます。

廃止は、バイナリとデザイン時の両方と互換性があります。 参照元のコードは引き続き正常に機能し、当座はアクションは必要ありません。 コンパイル時、非推奨の成果物への参照がコンパイル **警告** として報告されます。

## <a name="cleanup-of-deprecated-elements"></a>非推奨の要素のクリーンアップ

12 か月の期間後、Microsoft は古いメソッドおよびメタデータ要素を削除する可能性があります。

ただし、テレメトリが、古い形式のメソッドやメタデータ要素がまだ使用されていることを示す場合、Microsoft は、消費者の中断リスクを減らすため削除 **しません**。

## <a name="minimize-your-risk-of-being-affected"></a>影響を受けるリスクを最小限にする

ここでは、メソッドおよびメタデータ要素が非推奨になるときに受ける影響を避けるために、Microsoft のコード ベースの消費者が使用できるヒントを示します。

- 少なくとも 12 か月ごとに、コード ベースを最新のコード ベースでコンパイルします。 非推奨の成果物が使用されるために警告が表示される場合は、できるだけ早く警告を解決します。
- 非推奨の成果物での **新しい** 依存関係は避けてください。 リリースが利用可能になるタイミングとテレメトリが利用可能になるタイミングには時間差があるため、Microsoft は成果物を削除する可能性があります。

## <a name="list-of-deprecated-methods-and-metadata-elements"></a>非推奨のメソッドとメタデータの要素のリスト

参考のため、各メジャー リリースで非推奨としてマークされているアーティファクトを示した Microsoft Excel ファイル [ObsoleteElementsPerVersion.xlsx](https://mbs2.microsoft.com/fileexchange/?fileID=d6b5589b-c2c7-4cdd-a6b9-87e080cb2f05) をダウンロードします。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

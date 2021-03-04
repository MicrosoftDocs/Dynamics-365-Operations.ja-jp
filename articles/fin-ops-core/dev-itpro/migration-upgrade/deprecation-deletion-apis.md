---
title: 方法とメタデータの要素の廃止
description: このトピックでは、コード ベースの拡大に伴って古くなるメソッドよびメタデータ要素の廃止に関する情報が提供されます。
author: jorisdg
manager: AnnBe
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 6e89a66d72744547eb38707c9cdad17a700ad7f2
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154349"
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

参考のため、CustomerSource の[方法とメタデータの要素の廃止](https://docs.microsoft.com/dynamics/s-e/)ページにある Microsoft Excel ファイルをダウンロードしてください。各メジャー リリースで非推奨とマークされた成果物が示されています。

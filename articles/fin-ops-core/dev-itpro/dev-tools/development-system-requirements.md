---
title: 開発システム要件
description: このトピックでは、開発のシステム要件を一覧表示します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 33221
ms.assetid: f39dbe39-7dc3-463c-923e-f22af231b979
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b507900f9eb8d11d4dec1b79ed16b202ef9129f
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866350"
---
# <a name="development-system-requirements"></a>開発システム要件

[!include [banner](../includes/banner.md)]

このトピックでは、開発のシステム要件を一覧表示します。

開発環境は、ローカルまたは Microsoft Azure でホストできます。 ビルド プロセス、X++ コンパイル、および相互参照情報の生成は、通常、16 GB のメモリと 2 つの CPU コアを搭載したマシンで十分に動作します。 コンパイラではリソースを使用するため、特に同時プロセスからのリソースの競合がある場合、より多くの RAM とコアがコンパイルを高速化することができます。 同時プロセスを実行している場合は、4 つのコアで 24 GBのメモリをお勧めします。 同時に実行される可能性のあるコンポーネントが開発環境に多数含まれているので、少なくとも 2 つの CPU コアをお勧めします。 コンポーネントには、AOS Web アプリケーション、Visual Studio、Management Reporter および SQL Server が含まれます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
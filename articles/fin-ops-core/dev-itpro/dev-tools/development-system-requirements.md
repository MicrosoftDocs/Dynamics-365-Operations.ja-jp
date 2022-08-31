---
title: 開発システム要件
description: この記事では、開発のシステム要件を一覧表示します。
author: gianugo
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 33221
ms.assetid: f39dbe39-7dc3-463c-923e-f22af231b979
ms.openlocfilehash: fcf4d2311adf14ed3cbe6e0471618a6dbbdd4084
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271167"
---
# <a name="development-system-requirements"></a>開発システム要件

[!include [banner](../includes/banner.md)]

この記事では、開発のシステム要件を一覧表示します。

開発環境は、ローカルまたは Microsoft Azure でホストできます。 ビルド プロセス、X++ コンパイル、および相互参照情報の生成は、通常、16 GB のメモリと 2 つの CPU コアを搭載したマシンで十分に動作します。 コンパイラではリソースを使用するため、特に同時プロセスからのリソースの競合がある場合、より多くの RAM とコアがコンパイルを高速化することができます。 同時プロセスを実行している場合は、4 つのコアで 24 GBのメモリをお勧めします。 同時に実行される可能性のあるコンポーネントが開発環境に多数含まれているので、少なくとも 2 つの CPU コアをお勧めします。 コンポーネントには、AOS Web アプリケーション、Visual Studio、Management Reporter および SQL Server が含まれます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

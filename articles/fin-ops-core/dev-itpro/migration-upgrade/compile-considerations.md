---
title: 最新の更新プログラムに対してコードをコンパイルするための計画と準備
description: このトピックでは、最新の製品更新プログラムを使用してパートナー コードをコンパイルするときに、開発者が遭遇する可能性のある潜在的な問題を取り上げます。
author: dfroslie
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: Dynamics365Operations
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 102343
ms.assetid: e48d7424-371a-49ee-882c-07b7ceb00183
ms.search.region: Global
ms.author: dfroslie
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 05bc0afea37f14e19621df1383647ed0d1a37d83
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191886"
---
# <a name="plan-and-prepare-for-compiling-code-against-the-latest-update"></a>最新の更新プログラムに対してコードをコンパイルするための計画と準備

[!include [banner](../includes/banner.md)]

1 つのバージョンのサービス プランの展開では、Microsoft はバイナリおよび機能の観点から下位互換性の確保に努めています。 1 つのバージョンの詳細については、[1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-and-ops/get-started/one-version.md)を参照してください。 下位互換性が優先事項であっても、開発活動の結果コードの変更が必要になる状況があります。 そのような状況の一部を次に示します。 

- Microsoft が列挙を拡張可能にするとき、バイナリと互換性のある変更と見なされます。 コンパイラは、非拡張可能列挙の整数値に依存する安全ではない拡張可能列挙操作をチェックします。 安全ではない拡張可能列挙操作を含むすべてのパートナー コードは、再コンパイル時にコンパイラ エラーとなるため、変更を加える必要があります。 詳細については、[拡張機能による列挙への値の追加](../extensibility/add-enum-value.md)を参照してください。

- コンパイル時に生じる可能性のある未解決の参照を避けるため、パートナー モデルは最上位レベルのモジュールと下位のモジュールを参照する必要があります。 これを行わないと、参照されていない下位モジュールに新しいリソースを追加する Microsoft の変更により、未解決の参照が発生する可能性があります。 コンパイル エラーを解決するには、参照として下位モジュールを追加します。

- いくつかのメソッドは、将来完全に非推奨となることを示すため、非推奨属性が設定されます。 古いメソッドの呼び出しまたはラップのために生成されたコンパイラ警告は、予想されるコード パスがまだ存在することを確認するために調べる必要があります。 場合によっては、Microsoft コードが古いメソッドの代わりに新しいメソッドを直接呼び出します。 この場合、古いメソッドに基づいて構築されたコードは実行されません (予期される場合)。

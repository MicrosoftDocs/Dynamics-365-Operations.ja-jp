---
title: オンライン ストア カタログの公開
description: この記事には、Commerce モジュールからオンライン ストアにカタログを公開する方法を理解するための概念に関する情報が含まれています。
author: mugunthanm
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: AX 10.0.10
ms.openlocfilehash: e977f9a2e1b9031c75c803ff05e964bc4743cbb1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845880"
---
# <a name="publish-an-online-store-catalog"></a>オンライン ストア カタログの公開

[!include [banner](../includes/banner.md)]

この記事には、Commerce モジュールからオンライン ストアにカタログを公開する方法を理解するための概念に関する情報が含まれています。

## <a name="publish-an-online-store-catalog"></a>オンライン ストア カタログの公開

製品カタログを使用すると、オンライン ストアで提供する製品を識別できます。 カタログを作成するときは、製品が提供されるオンライン ストアを識別し、製品を追加し、販売促進の詳細の追加によって製品の提供を強化します。 カタログが承認された後、オンライン ストアで製品を使用できるようにカタログを公開します。 製品カタログを発行する前に、以下の設定タスクを実行する必要があります。

1. 製品を設定し、階層、品揃え、およびバリアントを構成します。
2. 製品カタログを設定し、属性グループおよびワークフローを構成します。

これらの手順を完了した後は、オンライン ストア カタログを公開する準備ができます。

1. Finances and Operations は、コマース データベース内の製品テーブルを読み取ります。
2. Async Server はチャネル データベースのすべての製品を同期します。
3. CRT/パブリッシュ コネクターは、*一覧* を作成します。 一覧は、特定の時点におけるチャネルの製品のインスタンスです。 たとえば、「ジーンズ」という名前の製品があり、この製品には「赤」という名前のバリアントがあります。 この場合、システムは「赤いジーンズ」の一覧を作成します。
4. システムは、リスティングに新しい属性が追加されたかどうかを判断します。 新しい属性が追加された場合 (例えば 「赤いジーンズ」 リストに **テクスチャ** という名前の新しい属性が含まれ、この属性がチャネル レベルで **組み込まれている** とマークされている場合)、システムにはこの属性のカスタム サイト内の列が作成されます。 また、リスト アイテムの新しいルールが作成され、「赤いジーンズ」リストの新しい行が作成され、SharePoint でプロセスが完了します。
5. CRT では、一覧の公開状況を記録します。
6. Async Server は、一覧の公開ステータスを他のすべての公開ステータスと同期します。 状態は、**公開済** または **エラー** のいずれかになります。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

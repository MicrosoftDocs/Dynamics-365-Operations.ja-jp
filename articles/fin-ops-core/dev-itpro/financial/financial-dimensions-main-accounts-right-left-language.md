---
title: 右から左へ読み書きする言語の財務分析コードと主勘定
description: このトピックでは、右から左へ読み書きする言語を使用する際に考慮する必要がある決定について説明し、財務分析コードと主勘定を設定する必要があります。
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2bdf1b99ae7be6c9d9c43c91c9273e18ce9b1093
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127650"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>右から左へ読み書きする言語での財務分析コードと主勘定

[!include [banner](../includes/banner.md)]

このトピックでは、右から左へ読み書きする言語を使用する際に考慮する必要がある実装の決定について説明し、財務分析コードと主勘定を設定する必要があります。

財務分析コードと主勘定は、実装のための計画フェーズの主要部分です。 財務分析コードと主勘定がシステムに作成されると、**勘定構造のコンフィギュレーション**、**詳細なルール構造**、**アプリケーション統合用の財務分析コードのコンフィギュレーション** ページで使用されます。 これらのページで定義された順序は、データ入力および消費のためにシステムで使用されます。 システムの一部の場所では、財務分析コードと主勘定は、別のフィールドに表示されます。 ただし、仕訳帳などの他の場所では、財務分析コードと主勘定は単一の文字列として表示されます。

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>右から左のシステムの財務分析コードと主勘定を設定するためのベスト プラクティス

- 勘定科目表の区切り記号を選択するときは、二重区切り記号オプションのうち 1 つを選択します: 二重ハイフン (`--`)、二重縦線 (`||`)、または 2 つのピリオド (`..`)、もしくは二重アンダースコア (`\\`)。
- 財務分析コードと主勘定の値を作成するときに、番号と右から左へ読み書きする言語文字のみを使用します。
- 財務分析コードと主勘定の値で選択した勘定科目表の区切り記号を使用することは避けてください。

これらのベスト プラクティスに従うことにより、システム全体のユーザー定義順序の一貫した表示を保証します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
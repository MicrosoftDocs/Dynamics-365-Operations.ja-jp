---
title: 財務諸表デザイナーでのレポート定義
description: この記事では、レポート定義に関する情報を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7d5531112cfb803912849af3af785b2a69a79f3d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093417"
---
# <a name="report-definitions-in-financial-report-designer"></a>財務諸表デザイナーでのレポート定義

[!include [banner](../includes/banner.md)]

この記事では、レポート定義に関する情報を示します。 レポート定義は、行定義、列定義、およびオプションのレポート ツリー定義を使用してレポートを作成するレポート コンポーネント (または構成要素) です。 レポート定義は、レポートをカスタマイズするためのオプションおよび設定も提供します。 

レポート定義は、行定義、列定義、およびオプションのレポート ツリー定義を使用してレポートを作成するレポート コンポーネント (または構成要素) です。 レポート定義は、レポートのカスタマイズに使用できるオプションおよび設定も提供しています。 行定義と列定義を定義したら、レポート定義に結合する必要があります。 この時点で、詳細レベルおよびレポートの日付などの定義の他の側面も定義します。 これで、レポートの保存および生成ができます。 財務諸表は、レポート用に次の詳細レベルを提供します。

- 財務
- [財務と勘定]
- [財務]、[勘定] および [トランザクション]

ただし、Microsoft Dynamics ERP システムにデータを格納する方法によって、トランザクションの詳細がレポートで使用できない場合があります。

## <a name="create-a-report-definition"></a>レポート定義の作成
1. [レポート デザイナー] の **ファイル** メニューで、**新規** をクリックし、**レポート定義** を選択します。
2. **レポート**、**出荷および配送**、**ヘッダーおよびフッター**、**設定** タブで、適切な情報を指定します。

## <a name="contents-of-a-report-definition"></a>レポート定義の内容
次の表は、レポート定義のタブと、情報の使用方法について説明します。

<table>
<thead>
<tr>
<th>タブ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr>
<td>レポート </td>
<td>レポートを作成し、レポートをコンフィギュレーションし、既存のレポートを変更します。</td>
</tr>
<tr>
<td>[出荷および配送]</td>
<td>レポートの出力のタイプと出力先を変更します。</td>
</tr>
<tr>
<td>[ヘッダーとフッター]</td>
<td>レポートのヘッダーおよびフッターを定義および書式設定します。 たとえば、ヘッダーまたはフッターにテキストや画像を追加できます。 財務諸表は、画像の .bmp、.jpg、.png ファイルをサポートします。 自動テキスト コードを追加して、会社名、レポート名、ページ番号などの他の情報を挿入できます。</td>
</tr>
<tr>
<td>設定</td>
<td>次の設定などのレポート定義の設定を指定します :
<ul>
<li>金額の書式設定および丸め</li>
<li>詳細レポートの書式設定</li>
<li>レポート ツリーの書式設定</li>
<li>例外レポートの生成</li>
<li>通貨換算の指定</li>
<li>小計およびフィルターの勘定の詳細</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>その他のリソース

[財務報告](financial-reporting-intro.md)

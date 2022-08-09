---
title: ドキュメント レポート サービス
description: この記事では、サービス管理が簡略化され、開発者の生産性が向上し、強化されたレポート表示を提供するレポート ソリューションについて説明します。
author: RichdiMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom:
- "69191"
ms.assetid: 57aaba22-4068-4c3f-9428-7fcd99632295
ms.openlocfilehash: b87910e5c01717f64db7e44f4021b825e100b0d2
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205879"
---
# <a name="document-reporting-services"></a>ドキュメント レポート サービス

[!include [banner](../includes/banner.md)]

この記事では、利用可能な統合レポート ソリューションについて説明します。 このソリューションにより、サービス管理が簡略化され、開発者の生産性が向上し、ユーザーのレポート表示エクスペリエンスが強化されます。

## <a name="document-reporting-services"></a>ドキュメントの Reporting Services

ドキュメント レポート サービス は、Microsoft SQL Server Reporting Services (SSRS) に基づいています。 アプリケーションの現在のバージョンで、これらのサービスは Microsoft Azure 計算サービスでホストされます。 1 ボックス環境で開発している場合は、サービスも Azure コンピューティング エミュレーターでローカルに実行されます。

### <a name="service-deployment--local-vs-cloud"></a>サービスの展開 - ローカルとクラウド

1 ボックス環境では、開発者は Microsoft Visual Studio を使用して、エンド ツー エンドでレポートを作成、変更、およびプレビューできます。 アプリケーションのメタデータ ストアにレポートを追加するために、別のプロセスは必要ありません。 レポートの変更は、他のソリューションの更新と一緒にパッケージ化され、ローカル環境での開発が完了した後にクラウドに展開されます。

### <a name="viewing-reports"></a>レポートを表示する 

エンド ユーザーに提供される拡張レポート表示エクスペリエンスは、Microsoft Visual Studio のレポート プレビュー エクスペリエンスと同じものです。 Visual Studio で個別のデザインのプレビューは以後使用しません。 代わりに、Ctrl+F5 を押すだけで、Internet Explorer ウィンドウでレポートを作成してプレビューできます。 レポートはクライアントに表示されるとおりに表示されます。 ユーザーのパラメーターの経験さえ同じです。 次の画像は、Visual Studio から開いたレポート プレビューの例を示しています。

[![レポート プレビューの例。](./media/2_report.png)](./media/2_report.png)

## <a name="service-administration-prerequisites"></a>サービス管理の前提条件
次のテーブルは、Microsoft Dynamics AX 2012 とアプリケーションの現在のバージョンのサービス管理の前提条件を比較しています。

<table>
<thead>
<tr>
<th>AX 2012</th>
<th>アプリケーションの現在のバージョン</th>
</tr>
</thead>
<tbody>
<tr>
<td>レポートの開発環境には、次の前提条件があります。
<ul>
<li>SSRS がインストールされている必要があります。</li>
<li>SSRS は、Reporting Services 構成マネージャーを使用して構成する必要があります。</li>
<li>アプリケーションの SSRS 拡張機能がインストールされている必要があります。</li>
</ul></td>
<td>Reporting Services は、アプリケーション サーバーとともに Azure コンピューティング エミュレーターで実行されます。 したがって、SSRS サービス管理の前提条件はありません。 レポートがローカル レポート作成サービスに配置された後は、クライアントからアクセスできます。</td>
</tr>
</tbody>
</table>

## <a name="developing-application-reports"></a>アプリケーションのレポートの開発
Visual Studio では、レポート ソリューションを完全に作成および検証できるので、現在のバージョンでレポートを作成するプロセスは AX 2012 で行うよりも簡単です。 次のテーブルは、アプリケーションがどのようにしてクエリに基づく自動設計レポートを追加するための基本手順を簡素化するかを示しています。

<table>
<thead>
<tr>
<th>AX 2012</th>
<th>アプリケーションの現在のバージョン</th>
</tr>
</thead>
<tbody>
<tr>
<td><ol>
<li>アプリケーションの、アプリケーション オブジェクト ツリー (AOT) でクエリを作成します。</li>
<li>Visual Studio で、レポート プロジェクトを作成してクエリを追加します。</li>
<li>Visual Studio モデル エディターでレポートを編集します。</li>
<li>モデル エディタ ツールバーを使用して Visual Studio でレポート デザインをプレビューします。</li>
<li>Visual Studio を使用して AOT にレポートを追加します。</li>
<li>クライアントの AOT を使用してレポートのメニュー項目を作成し、メニュー項目をメニューに追加します。</li>
<li>AOT を使用してレポートをレポート サーバーに展開します。</li>
<li>クライアントのレポートを確認します。</li>
</ol></td>
<td><ol>
<li>Visual Studio で、レポート プロジェクトとクエリを作成します。</li>
<li>Visual Studio でレポートを編集します。</li>
<li>Visual Studio で、メニュー項目にレポートを追加し、スタートアップ オブジェクトとしてメニュー項目を設定します。</li>
<li>AOT を使用してレポートをレポート サーバーに展開します。</li>
<li>Ctrl+F5 キーを押して、アプリケーションのレポートを確認します。
<blockquote>[!NOTE] モデル エディタからのレポート デザインの個別のプレビューはありません。</blockquote>
</li>
<li>ソリューション全体が完了したら、ソリューション全体を 1 つのパッケージにしてクラウドに配置します。</li>
</ol></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

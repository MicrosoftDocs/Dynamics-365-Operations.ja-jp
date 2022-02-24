---
title: 分割されたモデル
description: このトピックでは、スタックの 3 つの主要モデル、つまりアプリケーション プラットフォーム、アプリケーション基盤、アプリケーション スイートへの分割について説明します。
author: maertenm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26941
ms.assetid: feaa09c5-efc7-4594-921e-b42536b18852
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79fb6dfba946458475d0b74a1d6630a73b6da1f4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408835"
---
# <a name="model-split"></a>分割されたモデル

[!include [banner](../includes/banner.md)]

このトピックでは、スタックの 3 つの主要モデル、つまりアプリケーション プラットフォーム、アプリケーション基盤、アプリケーション スイートへの分割について説明します。

## <a name="overview"></a>概要

モジュール コードを開発することは、モデル分割の原動力です。 複数のモデルにスタックを分割すると、コンパイル時間の短縮、実稼動環境でのパートナー IP の適切な区別など、多くの利点が提供されます。 メイン モデルは、**アプリケーション プラットフォーム**、**アプリケーション基盤**、**アプリケーション スイート** の 3 つがあります。 

[![First\_ModelSplit](./media/first_modelsplit.png)](./media/first_modelsplit.png) 

<strong>アプリケーション プラットフォーム</strong>は最下位モデルであり、カーネルとやり取りする最下位レベルの要素が含まれています。 **アプリケーション オブジェクト サーバー** (**AOS**) は、 **アプリケーション プラットフォーム** を使用してのみ起動できます。 **アプリケーション基盤** は、**アプリケーション プラットフォーム** の一番上に配置され、すべてのアプリケーションによって共有されるフレームワーク機能を含みます。 最後に、**アプリケーション スイート** は **アプリケーション基準** の上部に位置し、アプリケーションの特定要素を含みます。 付録のモデル内訳表は、これらの各モデルのコンポーネントの例を示します。 各モデルは、独自のアセンブリにコンパイルされ、下位レイヤー モデル アセンブリに依存します。 **アプリケーション プラットフォーム** は、他のモデルには依存しません。 これは、モデルをアセンブリに直接マッピングすることを意味します。 

[![ModelAssembly\_ModelSplit](./media/modelassembly_modelsplit1.jpg)](./media/modelassembly_modelsplit1.jpg) 

モジュール スタックで開発することで、**アプリケーション スイート** で変更を行い、残りのスタックに触れることなくコンパイルすることができます。 新しい変更のあるモデルのみコンパイルされる必要があり、コンパイルの時間が大幅に短縮されます。 詳細については、この記事の終わりにある「モデルの内訳」セクションで確認できます。

## <a name="customizing-models"></a>モデルのカスタマイズ
カスタマイズの方法には、オーバーレイと拡張の 2 種類があります。 オーバーレイヤーにより、下位レベルでモデル内の要素を変更、つまりオーバーレイする複数のレイヤーに変更を加えることができます。 拡張子を使用すると、要素のイベントやプラグイン ポイントに新しい要素を追加したり、コードをアタッチすることができます。 使用されるカスタマイズのタイプは、モデルがどのようにコンパイルされ、最終的にパッケージ化されるかに影響を与えます。 1 つ以上のモデルが、アセンブリにコンパイルされます。 アセンブリ、非コード メタデータ、およびそれをコンパイルされたコンポーネントはパッケージを形成します。 パッケージは、独立した配置可能な単位です。 拡張機能のカスタマイズのみが含まれるモデルは、独自のアセンブリにコンパイルして独自のパッケージに配置できます。 任意のオーバーレイが含まれるモデルは、オーバーレイ モデルに基づいてアセンブリにコンパイルする必要があります。 

[![カスタマイズ アセンブリ](./media/customization-assemblies.png)](./media/customization-assemblies.png)   

拡張機能の使用には、以下を含むいくつかの利点があります。

-   アプリケーション ライフ サイクル管理の目的で、拡張コンポーネントのみを管理する必要があります。
-   カスタマイズの構築ではアプリケーション全体を再コンパイルする必要はありません。
-   クラウドで Microsoft はユーザーのカスタマイズに影響を与えずに、インストール、パッチ、アップグレード、および内部 API の変更を行えます。
-   他のカスタマイズを意識せずに、ソリューションを別々に処理することができます。

現在、コード拡張、テーブル拡張、フォーム拡張、メニュー拡張、列挙拡張がサポートされています。 [拡張機能およびオーバーレイによるカスタマイズ](../extensibility/customization-overlayering-extensions.md) と [拡張機能によるモデル要素のカスタマイズ](../extensibility/customize-model-elements-extensions.md) の拡張機能セクションでは、拡張機能の使い方について詳しく説明しています。  拡張子は、可能な限りサポートされている要素で使用する必要があり、既存の Microsoft コードを変更する必要がない場合に最適です。 メソッドの機能をマスクするための変更には、コード自体を変更するためのオーバーレイが必要です。  オーバーレイヤーは、カスタマイズが基本機能をカスタマイズする場合に、拡張機能がカバーしない領域に存在する必要があります。 次の図は、2 つのカスタマイズ戦略の違いをまとめたものです。 

[![カスタマイズの概要](./media/customization-overview.png)](./media/customization-overview.png)

## <a name="model-breakdown"></a>モデルの内訳
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>モデル</strong></td>
<td><strong>概念</strong></td>
</tr>
<tr class="even">
<td>アプリケーション プラットフォーム</td>
<td>アプリケーション ロジックに対応するカーネル機能へのアプリケーション プラットフォーム インターフェイス。 AOS は、このモデルだけで開始することができます。
<ul>
<li>AIF 基準オブジェクト</li>
<li>バッチ</li>
<li>フォーム基本対象</li>
<li>RunbaseSysOperations* ベース オブジェクト</li>
<li>DictXX オブジェクト</li>
<li>Appl、情報、グローバル、ClassFactory</li>
<li>データ アクセス オブジェクト</li>
<li>ヘルパー クラス</li>
<li>ENUM/EDT/Macros/ConfigKey/LicenseCode</li>
</ul></td>
</tr>
<tr class="odd">
<td>アプリケーション基準</td>
<td><ul>
<li>アプリケーション基準機能:
<ul>
<li>フレームワーク分析コード</li>
<li>グローバル アドレス帳</li>
<li>番号順序</li>
<li>OrgModel</li>
</ul></li>
<li>機能領域:
<ul>
<li>ビジネス インテリジェンス</li>
<li>レポート</li>
<li>アップグレード フレームワーク</li>
<li>セキュリティ</li>
<li>電子署名</li>
<li>データのインスポート/エクスポート</li>
<li>ワークフロー</li>
</ul></li>
<li>SYS オブジェクト:
<ul>
<li>ベスト プラクティス</li>
<li>チェックリスト</li>
<li>保険証書</li>
<li>RecordTemplate</li>
</ul></li>
<li>その他:
<ul>
<li>通貨</li>
<li>測定単位</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Application Suite</td>
<td><ul>
<li>サプライ チェーン マネジメント</li>
<li>人材管理</li>
<li>プロフェッショナル サービスなど</li>
</ul></td>
</tr>
</tbody>
</table>






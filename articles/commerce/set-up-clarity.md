---
title: Dynamics 365 Commerce での Microsoft Clarity の設定
description: このトピックでは、Dynamics 365 Commerce 環境内で Microsoft Clarity を設定する方法について説明します。
author: BrianShook
ms.date: 01/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2021-01-25
ms.dyn365.ops.version: ''
ms.openlocfilehash: a35c7cc064154ecd3ef62f17ae3592b4473f5e35
ms.sourcegitcommit: 7fc0a9a6440ac087292e9e76c26c67f56154b9e6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2022
ms.locfileid: "8051384"
---
# <a name="set-up-microsoft-clarity-in-dynamics-365-commerce"></a>Dynamics 365 Commerce での Microsoft Clarity の設定

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Commerce 環境内で Microsoft Clarity を設定する方法について説明します。 

[Microsoft Clarity](https://clarity.microsoft.com/) は、サイト所有者が自分の e コマース サイトとのユーザー操作を理解するのに役立つユーザー動作分析ツールです。 Clarity の分析ツールは、セッション記録、ヒートマップ、および機械学習情報を使用して可視性を実現し、ユーザー操作を確認及び調査します。 

Clarity を Dynamics 365 Commerce サイトに統合するのは簡単です。このトピックの手順に従うだけで、Clarity がユーザー操作を詳細に確認できるようになります。

## <a name="sign-up-for-clarity"></a>Clarity にサインアップします

Clarity にサインアップするには、[Clarity](https://clarity.microsoft.com/) Web サイトに移動して **開始** を選択します。 設定プロセス中に、Commerce サイトに関連付けられた実稼働環境ドメイン URL を使用します。 Clarity 設定の詳細については、[はじめに](/clarity/getting-started) を参照してください。

## <a name="integrate-clarity-with-your-commerce-site"></a>Clarity を Commerce のサイトに統合する

Clarity にサインアップした後、Commerce のサイト ビルダで次の手順に従って、Clarity を e コマース サイトに統合します。

### <a name="configure-content-security-policy-for-clarity"></a>Clarity のコンテンツ セキュリティ ポリシーの構成

コンテンツ セキュリティ ポリシー (CSP) は、サイトページの読み込みが許可されているリソースを制御するのに役立つ広範なポリシー ディレクティブのセットを提供します。 各ディレクティブは、特定のタイプのリソースに対する制限を定義します。 Clarity をサイトで機能させるには、Clarity リソースを呼び出すことができるように一部の CSP ディレクティブを構成する必要があります。 

Commerce サイト ビルダーで Clarity を構成するには、次の手順に従います。

1. Commerce サイトに移動します。
1. **サイト 設定 \> 拡張機能** を選択します。
1. **コンテンツ セキュリティ ポリシー** タブを選択します。
1. **child-src** ディレクティブ セクションで、**追加** を選択します。
1. **``https://www.clarity.ms``** を入力します。
1. **connect-src** および **script-src** ディレクティブについて、手順 4 と 5 を繰り返します。
1. **保存と公開** を選択します。

### <a name="embed-clarity-tracking-script-code-into-site-pages"></a>Clarity トラッキング スクリプト コードをサイト ページに埋め込む

Clarity で追跡する Commerce サイト ページに、Clarity 追跡スクリプト コードを埋め込むことができます。

開始するには、Clarity ポータルからプロジェクトの追跡スクリプト コードをコピーします。 次に、Clarity 追跡スクリプト コードを Commerce モジュール ライブラリ *インライン スクリプト モジュール* に追加する必要があります。 構成によっては、インライン スクリプト モジュールを特定のサイト ページに直接追加することも、サイト ページのテンプレートで許可されるオプションとして追加する必要がある場合があります。 

> [!NOTE]
> Clarity 追跡スクリプト コードをインライン スクリプト モジュールにコピーする時に、文字列から周囲の **\<script\>** タグを削除できます。 インライン スクリプト モジュールは、ページまたはフラグメントが公開および表示されるときに、必要な **\<script\>** タグを追加します。

サイト ページの範囲に Clarity 追跡スクリプト コードを含めるのが最も効率的な方法は、共有サイト ページ テンプレートにスクリプト コードを埋め込む方法です。 次の手順では、サイト ページ テンプレートで使用するインライン スクリプト モジュールを含むフラグメントに Clarity スクリプト コードを挿入する方法について説明します。 

Clarity 追跡コードを Commerce サイト ビルダーのサイト ページに埋め込むには、次の手順に従います。

1. Commerce サイト ビルダーでサイトに移動します。
1. **フラグメント** を選択し、**新規** を選択します
1. **新規フラグメント** ダイアログ ボックスで、**インライン スクリプト** モジュールを選択します。
1. **フラグメント名** に名前を入力し、**OK** を選択します。
1. **既定のインライン スクリプト** モジュール スロットを選択し、モジュールのプロパティ ペインで、**インライン スクリプト** の下の Clarity スクリプトに貼り付けます。 スクリプト文字列をコピーした場合は、周囲の **\<script\>** タグを必ず削除してください。
1. **保存** を選択してから、**発行** を選択します。
1. **テンプレート** を選択し、Clarity スクリプト コードを含むフラグメントを追加するテンプレートを選択します。
1. **編集** を選択します。
1. **HTML Head** スロットの省略ボタン (...) を選択し、**フラグメントの追加** を選択します。
1. **フラグメントの選択** ダイアログ ボックスで、Clarity スクリプト コードの付いた新しいフラグメントを選択し **OK** を選択します。 フラグメントが **HTML ヘッド** スロットの下に表示されることを確認します。
1. **保存** を選択してから、**発行** を選択します。 更新したテンプレートを使用するすべてのサイト ページに、Clarity スクリプト コードが埋め込まれます。
1. Clarity スクリプトコードを追加する追加のテンプレートは、必要に応じて前の手順を繰り返します。

Clarity スクリプトがサイト ページに埋め込まれているかどうかをテストする方法については、[Clarity セットアップ: 検証](/clarity/clarity-setup#verification) を参照してください 。

### <a name="embed-clarity-tracking-script-code-into-a-specific-site-page"></a>Clarity 追跡 スクリプト コードを特定のサイト ページに埋め込みます

> [!NOTE] 
> インライン スクリプト モジュールは Clarity スクリプト コードをページ インスタンスに追加できるように、ページのテンプレートの **HTML ヘッド** セクションに存在している必要があります。

Clarity 追跡コードを Commerce サイト ビルダーの特定のサイト ページに埋め込むには、次の手順に従います。

1. Commerce サイト ビルダーでサイトに移動します。
1. **ページ** を選択し、Clarity スクリプト コードを追加するページを選択し、**編集** を選択します。
1. モジュールのアウトライン ペインでルート ノード スロットを選択します。
1. **SEO プロパティ** の下のプロパティ ペインで、**スクリプト タグ** セクションを展開します。 **インライン スクリプト** の下に、Clarity 追跡コードを貼り付けます。 スクリプト文字列をコピーした場合は、周囲の **\<script\>** タグを必ず削除してください。
1. **保存** を選択し、**編集を終了する** を選択し、続いて **公開** を選択します。

Clarity スクリプトがサイト ページに追加された後、Clarity ポータルででデータとキャプチャの表示を開始する必要があります。 結果を表示する前に、ページ ビューを累積するために追加の時間が必要な場合があります。

## <a name="additional-resources"></a>追加リソース

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)


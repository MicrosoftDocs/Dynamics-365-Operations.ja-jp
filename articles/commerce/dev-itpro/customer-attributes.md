---
title: 顧客属性
description: このトピックでは、顧客属性に関する情報を提供し、構成を使用して顧客のマスター レコードに新しいフィールドを追加する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 54880ca9c082e50283d2637283f8571e61ab4320
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004586"
---
# <a name="customer-attributes"></a>顧客属性

[!include [banner](../../includes/banner.md)]

顧客、顧客の注文、現金売りトランザクション、およびコール センター注文の属性をサポートするために、バックオフィスの属性フレームワークを拡張しました。

> [!NOTE]
> 属性は読み取り専用です。 ただし、顧客や注文属性の場合は、個々の顧客または注文のレベルで値を編集および設定できます。

新しい顧客属性フレームワークでは、コンフィギュレーションを使用して顧客マスター レコードに新しい項目を追加することができます。 これらのフィールドは販売時点管理 (POS) またはバックオフィスの **顧客の追加/編集**または**顧客の詳細**画面に自動的に表示されます。 コマース パラメーターの顧客属性グループを構成すると、POS とバックオフィスは自動的に新しい属性を表示します。 コードの変更またはカスタマイズは必要ありません。 また、画面レイアウト デザイナーを使用して、POS トランザクション画面に顧客の属性が表示されるように顧客カードを構成することができます。

## <a name="why-and-when-you-should-configure-customer-attributes"></a>顧客属性の構成が必要な理由および場合

顧客のマスター レコードに新しいフィールドを追加して、POS またはバック オフィスで情報を取得する場合は、この機能を使用できます。 以前は、顧客マスター レコードに新しいフィールドを追加して POS およびバックオフィスに表示するには、バックオフィスおよびチャネル データベースで新しい拡張テーブルを作成し、Commerce runtime (CRT) および POS コードでインライン変更を加える必要がありました。 拡張フィールドへの読み取り/書き込みを行い POS で表示するには、CRT および POS でコードを記述する必要がありました。 **顧客の詳細** 画面およびトランザクション画面の **顧客** パネルなど、さまざまな POS ビューやシナリオでこれを処理する必要がありました。 さらに、CRT で、挿入、選択、および更新のすべての操作を処理する必要があります。 ただし、新しい機能によりこれらのすべての手順をコンフィギュレーションによって完了できるため、コードを記述またはカスタム拡張機能テーブルを作成する必要はありません。

この機能の最初のバージョンは、**datetime** および **reference** 属性タイプをサポートしていません。 それらの属性タイプについては、POS に詳細を表示するのに、拡張機能プロパティおよびカスタム コントロールを使用する必要があります。

## <a name="configure-customer-attributes-in-pos-and-headquarters"></a>POS およびバックオフィスで顧客属性をコンフィギュレーション

### <a name="define-attribute-types"></a>属性タイプを定義

1. **製品情報管理** > **設定** &gt; **カテゴリと属性** > **属性タイプ** の順に選択します。
2. **属性タイプ**ページで、**新規**を選択し、新しい属性タイプを追加します。
3. 階層タイプ名を入力します。
4. **一般**クイック タブの、**タイプ**フィールドで、このデータ型に割り当てられている属性に入力できるデータのタイプを選択します。
5. 属性タイプが**少数点**または**整数**の場合、測定単位を選択します。
6. 属属性タイプの固定値リストを定義するには、**固定値リスト** チェック ボックスをオンにします。 次に、**値** クイックタブで、値のリストを追加します。

    > [!NOTE]
    > **固定リスト** チェック ボックスは、**テキスト** 属性タイプでのみ使用できます。

    または、属性タイプに有効な値の範囲を定義するには**値の範囲**チェック ボックスを選択します。 次に、**範囲** クイックタブで、値の有効範囲を入力します。

### <a name="define-attributes"></a>属性の定義

1. **製品情報管理** > **設定** > **カテゴリと属性** > **属性**の順に選択します。
2. **属性**ページで、**新規**を選択し、新しい属性を追加します。
3. 属性にユーザーを表示する必要がある名前、フレンドリ名、説明、およびヘルプ テキストを入力します。
4. **属性タイプ** フィールドで、属性に割り当てる属性タイプを選択します。
5. 属性タイプに応じて、**既定値**フィールドに、この属性が顧客に割り当てられたときに既定で表示される値または値の範囲を入力します。
6. **翻訳** を選択して **テキスト翻訳** ページ を開き、追加の言語で属性の名前、説明、フレンドリ名、およびヘルプ テキストを入力できます。
7. ステップ 2 ～ 6 を繰り返してさらに属性を追加します。

### <a name="define-an-attribute-group"></a>属性グループの定義

1. **製品情報管理** > **設定** > **カテゴリと属性** > **属性グループ**の順に選択します。
2. **属性グループ**ページで、**新規**を選択し、新しい属性グループを追加します。
3. 名前を入力し、次に**一般** FastTab で、属性グループのフレンドり名、説明、およびヘルプ テキストを入力します。
4. **属性**クイック タブで、**追加**を選択して、属性グループに属性を追加します。 **既定値**フィールドでは、選択した属性の既定値を入力できます。
5. **翻訳** を選択して **テキスト翻訳** ページ を開き、追加の言語で属性グループの説明、フレンドリ名、およびヘルプ テキストを入力できます。

### <a name="link-the-attribute-group-to-the-customers"></a>属性グループの顧客へのリンク

1. **Retail とコマース** > **バックオフィス設定** > **パラメーター** > **コマース パラメーター**の順に選択します。
2. **一般**タブの、**顧客属性グループ**フィールドに、属性グループ POS に表示する必要がある属性グループを選択します。

### <a name="run-the-distribution-jobs"></a>配送ジョブを実行

1. **Retail とコマース** > **Retail と コマース IT** > **配送スケジュール**の順に選択します。
2. **顧客** ジョブ (1010) を選択し、アクション ペインで **今すぐ実行** を選択します。 メッセージが表示されたら、**はい** を選択します。
3. **グローバル構成** ジョブ (1110) を選択し、アクション ペインで **今すぐ実行** を選択します。 メッセージが表示されたら、**はい** を選択します。

### <a name="view-customer-attributes"></a>顧客属性の表示

#### <a name="headquarters"></a>バックオフィス

1. **Retail とコマース** > **顧客** > **すべての顧客**の順に選択します。
2. アクション ウィンドウの **Retail とコマース** にある、**属性**セクションで、**小売属性**を選択して属性値を表示または編集します。

#### <a name="pos"></a>POS

- POS を起動し、**顧客の追加/編集** 画面を開いて顧客の属性値を設定または更新するか、**顧客の詳細** 画面を開いて構成されている属性を表示します。

### <a name="show-customer-attributes-in-the-pos-transaction-screen"></a>POS トランザクション画面に顧客属性を表示

#### <a name="headquarters"></a>バックオフィス

1. **Retail と Commerce** > **チャネル設定** > **POS 設定** > **POS** > **画面レイアウト**の順に選択します。
2. **画面レイアウト**ページで、**新規**を選択し新しい画面レイアウトを作成するか、既存の画面レイアウトを選択します。
3. スクリーン レイアウトの名前と ID を入力します。
4. **レイアウト サイズ**クイック タブで、**追加**ボタン選択して、POS の新しいレイアウト サイズを追加します。
5. **名前**フィールドで POS 画面の解像度を選択します。
6. **レイアウト サイズ**クイック タブで、**レイアウト デザイナー**ボタンを選択します。
7. プロンプトが表示されたら、**インストール/実行**ボタンを使用して Retail Designer Host をダウンロードしてインストールするには、**はい**を選択します。
8. 入力を求めるメッセージが表示されたら、Microsoft Dynamics 365 のユーザー名とパスワードを入力して、デザイナーを起動します。
9. デザイナーが開始された後、**顧客**カードを画面レイアウト デザイナーの任意の場所にドラッグします。
10. **顧客** カードを右クリックし、**カスタマイズ** を選択します。
11. **カスタマイズ - 顧客** カードのページが表示されたら、**利用可能な列** セクションで必要な属性を選択してから、右矢印ボタン (**>**) を選択して 、それらを **選択された列** セクションに移動します。 **上** または **下** ボタンを選択することにより、属性を上または下に移動することができます。
12. 完了したら、**OK** を選択して、変更を保存します。
13. 右上隅の**閉じる**ボタン (**X**) を選択し、画面レイアウト デザイナーを閉じます。 メッセージが表示されたら、**はい** を選択して、変更を保存します。
14. **Retail とコマース** &gt; **Retail とコマース IT** &gt; **配送スケジュール**の順に選択します。
15. **レジスター** ジョブ (1090) を選択し、アクション ペインで **今すぐ実行** を選択します。 メッセージが表示されたら、**はい** を選択します。

#### <a name="pos"></a>POS

1. POS を起動し、顧客をトランザクションに追加します。
2. トランザクション画面を開いて、追加された属性を表示します。
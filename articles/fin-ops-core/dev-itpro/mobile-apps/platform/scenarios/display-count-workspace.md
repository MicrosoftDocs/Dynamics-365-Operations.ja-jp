---
title: フィールドに数を表示
description: この記事では、正確で、迅速に表示される数を計算する方法について説明します。
author: jasongre
ms.date: 05/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.custom: 255544
ms.assetid: ''
ms.openlocfilehash: 5dd30aed6c57848c17f18273f19979c179b2a181
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286698"
---
# <a name="show-counts-in-fields"></a>フィールドに数を表示

[!include [banner](../../../includes/banner.md)]
[!include [mobile app deprecated](../../../includes/mobile-app-deprecation-banner.md)]

**pageLink** コントロールを使用してカウント (合計) を表示することができますが、行数をカウントする前にターゲット ページが読み込まれるため遅くなることがあります。 また、取得される行の数に制限があるため、計算される数は正しくない可能性があります。

![カウントを表示するタイルを持つワークスペース。](media/optimizing-workspace/Tiles_Original.png)

モバイル ワークスペースをより迅速に動作させる場合は、通常のフィールドを使用してカウントを表示し、そのフィールドをモバイル クライアントの **pageLink** コントロールとしてモデル化することをお勧めします。

次の例では、フリート管理アプリを使用しています。 フリート管理アプリでは、ワークスペースに顧客、予約、および車両の合計数が表示されます。 以前は、これらのカウントはターゲットとして AllCustomers、AllReservations、および AllVehicles を持っていた **pageLink** コントロールに起因していました。 **pageLink** コントロールは行を読み込み、カウントを実行しました。 (この方法は、推奨される方法ではありません。)

推奨される方法を使用するようワークスペース ページをコンフィギュレーションするには、これらの手順に従います。

1. サーバーで、サーバー上のフィールドを含む新しいフォームを作成します。 (既存のフォームに新しいフィールドを追加することもできます。) 次の図では、3 つのフィールドがある新しい **FMMobSummary** フォームが作成されます。

    ![3 つのフィールドを含むフォーム。](media/optimizing-workspace/FMMobSummary.png)

2. **FMMobSummary** フォームのモバイル アプリ デザイナーを使用してページを作成します。

    ![デザイナーでの新しいページ。](media/optimizing-workspace/NewPageInDesigner.png)

3. フィールドを **pageLink** コントロールに変換する業務ロジックを更新します。 フィールドにナビゲーション ターゲットを追加するには **configureControl** メソッドを使用します。 フィールドは、次に **pageLink** コントロールとして設定されます。 **configureControl** メソッドの引数は、ページ名、コントロール名、および更新が必要なプロパティのオブジェクトです。
4. ワークスペースのデザインを更新します。 ワークスペース ページの一部として概要ページを埋め込みします。 **pageLink** コントロールとして構成されるようになったフィールドを参照します。 スタイルを提供して **showCount:true** プロパティを設定し、カウントが **pageLink** コントロールに表示されるようにします。

    ![ビジネス ロジックの変更。](media/optimizing-workspace/ChangesToBL.png)

この方法を使用することにより、**pageLink** コントロールのローカライズされたラベルも取得します。 ワークスペースが読み込まれると、結果ははるかに高速になります。



[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]

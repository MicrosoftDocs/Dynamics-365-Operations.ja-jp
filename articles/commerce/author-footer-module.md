---
title: フッター モジュール
description: この記事では、フッター モジュール、および Dynamics 365 Commerce での作成方法について説明します。
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fefeed37ba0d0e800b9cd3cefcf207cde9a625d8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282960"
---
# <a name="footer-module"></a>フッター モジュール  

[!include [banner](includes/banner.md)]

この記事では、フッター モジュール、および Microsoft Dynamics 365 Commerce での作成方法について説明します。

フッター モジュールは、ページ フッターに表示されるモジュールをホストするために使用される特別なコンテナーです。 たとえば、**お問い合わせ** や **店舗ポリシー** ページなど、サイト内のさまざまなページへのリンクを含めることができます。

以下の図は、サイトのページにおけるフッター モジュールの例を示しています。

![フッター モジュールの例。](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>フッター モジュール プロパティ 

ほとんどのコンテナーと同様に、フッター モジュールでは見出しと幅のプロパティに対応しています。 また、複数のフッター カテゴリ モジュールの追加もサポートされています。 追加された各フッター カテゴリ モジュールは、フッター モジュールの列としてレンダリングされます。

## <a name="modules-available-in-a-footer-module"></a>フッター モジュールで使用できるモジュール

**フッター項目** – フッター項目モジュールには、ヘッダー、画像、およびリンクを含めることができます。 通常、ヘッダーはフッター セクションのタイトルとして使用されます。  フッター内のすべてのリンクは、テキストのみ (「お問い合わせ」や「プライバシー」リンクなど)、またはテキストと画像 (ソーシャル メディア リンクなど) の両方を持つようにコンフィギュレーションできます。 ヘッダーとリンクの両方が指定されている場合、ヘッダー プロパティはリンクに優先されます。 

**トップに戻る** – トップに戻るモジュールは、ページの上部にすばやく移動するためのリンクを提供します。 行先が必要です。 既定値は \# です。この値はユーザーをページの先頭に移動します。

## <a name="create-a-footer-module"></a>フッター モジュールの作成

1. **フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。
1. **フラグメントの選択** ダイアログ ボックスで、**コンテナー** モジュールを選択し、フラグメントの名前を入力して、**OK** を選択します。
1. **既定のコンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの選択** ダイアログ ボックスで、**フッター カテゴリ** モジュールを選択し、続いて **OK** を選択します。
1. **フッター カテゴリ** スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの選択** ダイアログ ボックスで **フッター項目** モジュールを選択して、**OK** を選択します。
1. 右側のプロパティ ウィンドウで **フッター項目** スロットを選択し、必要に応じて見出し、リンクとリンク テキスト、画像を構成します。
1. フッター項目を追加する場合は、手順 5 から 7 を繰り返します。
1. フッターに "トップに戻る" リンクを追加するには、**フッター カテゴリ** スロットの省略記号ボタン (**...**) を選択し、続いて **モジュールの追加** を選択します。
1. **モジュールの選択** ダイアログ ボックスで **トップに戻る** モジュールを選択して、**OK** を選択します。
1. 右側のプロパティ ウィンドウで **トップに戻る** スロットを選択し、必要に応じてテキストやその他のモジュール プロパティを構成します。
1. **編集の完了** を選択してフラグメントにチェックインし、 **発行** を選択して公開します。

すべてのページにヘッダーが表示されることを保証するには、サイトに対して作成されたすべてのページ テンプレートで次の手順を実行します。

1. **既定ページ** モジュールの **フッター** スロットに、作成したフッター フラグメントを追加します。
1. **編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。

ページ テンプレートにフラグメントを追加することにより、フッターがすべてのページにレンダリングされるようになります。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[コンテナー モジュール](add-container-module.md)

[購入ボックス モジュール](add-buy-box.md)

[カート モジュール](add-cart-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[注文確認モジュール](order-confirmation-module.md)

[ヘッダー モジュール](author-header-module.md)

[フッター モジュール](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

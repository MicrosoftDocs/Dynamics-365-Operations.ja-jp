---
title: テキスト ブロック モジュール
description: この記事では、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 9e422c203d719b2e46620ce50b9d029e7ebd8d4c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270485"
---
# <a name="text-block-module"></a>テキスト ブロック モジュール

[!include [banner](includes/banner.md)]

この記事では、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

テキスト ブロック モジュールは、テキスト コンテンツを追加するために使用されるモジュールです。 このコンテンツは、情報提供またはプロモーションです。

テキスト ブロック モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。 これらは、ページ コンテキストやその他の任意のモジュールに依存しないスタンドアロン モジュールです。

## <a name="examples-of-text-block-modules-in-e-commerce"></a>E コマースのテキスト ブロック モジュールの例

テキスト ブロック モジュールは、次の方法で使用できます。

* 製品の詳細ページで製品機能について紹介します。
* 任意のページで情報提供を目的とします。 たとえば、ロイヤルティ プログラムの利点を説明し、出荷ポリシーと返品ポリシーを説明し、よく寄せられる質問に回答し、または "弊社について" コンテンツを提供したりできます。
* 製品の詳細ページでカスタム メッセージを追加します。 (たとえば、"$50 以上のご注文で送料無料")。
* 製品の詳細ページ、カート ページ、チェックアウト ページ、およびその他のページで免責事項や連絡先の詳細を提供します (たとえば、"出荷および返品には店舗ポリシーが適用されます") 。

以下の図は、ホームページ上のテキスト ブロック モジュールの例を示しています。

![テキスト ブロック モジュールの例。](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>テキスト ブロック モジュール プロパティ

| プロパティ名     | 先頭値                                            | 説明 |
|-------------------|--------------------------------------------------|-------------|
| リッチ テキスト         | リッチ テキスト                                        | 段落のテキスト。 太字、下線付き、斜体など、基本的なリッチ テキスト機能がいくつかサポートされます。 |
| カスタム クラス名 | カスケード スタイル シート (CSS) クラス名        | 開発者がこのモジュールをフォーマットするために提供するカスタム CSS クラス名。 クラス名は、テーマ パックで定義する必要があります。 |
| フォント サイズ         | **小**、**中**、**大**、または **特大** | コンテンツのフォント サイズ。 |

## <a name="add-a-text-block-module-to-a-page"></a>テキスト ブロック モジュールをページに追加する

新しいページテキスト ブロック モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。

1. **テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。
1. **テンプレート名** 配下の **新規テンプレート**  ダイアログ ボックスに、**コンテンツ テンプレート** を入力します。
1. **本文** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの選択** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。
1. **保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。
1. **ページ** に移動し、**新規** を選択して新たなページを作成します。
1. **新規ページの作成** ダイアログ ボックスの **ページ名** に **コンテンツ ページ** と入力し、**次へ** を選択します。
1. **テンプレートの選択** で、作成した **コンテンツ テンプレート** を選択して **次へ** を選択します。
1. **レイアウトの選択** でページ レイアウト (例: **柔軟性の高いレイアウト**) を選択し、**次へ** を選択します。
1. **確認して終了** でページ構成を確認します。 ページ情報の編集が必要な場合は **戻る** を選択します。 ページ情報が正しい場合は **ページの作成** を選択します。 
1. 新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの選択** ダイアログ ボックスで **コンテナー** モジュールを選択して、**OK** を選択します。
1. コンテナー モジュールのプロパティ ウィンドウで、**幅** プロパティを **全コンテナー** に設定します。
1. **コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. **モジュールの選択** ダイアログ ボックスで **テキスト ブロック** モジュールを選択して、**OK** を選択します。 
1. テキスト ブロック モジュールのプロパティ ウィンドウで、**リッチ テキスト** フィールドにテキストを追加します。
1. **保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。
1. **編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[プロモーション バナー モジュール](add-alert.md)

[カルーセル モジュール](add-carousel.md)

[コンテンツ ブロック モジュール](add-hero-module.md)

[ビデオ プレーヤー モジュール](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

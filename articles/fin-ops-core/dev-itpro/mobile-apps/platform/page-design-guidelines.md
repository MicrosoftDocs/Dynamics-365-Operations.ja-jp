---
title: ページ デザインのガイドライン
description: このトピックでは、モバイル アプリのページ デザインのガイドラインを提供します。
author: tonyafehr
ms.date: 05/26/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.custom: intro-internal
ms.author: tfehr
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: b1919bc0122d7cdc79baf1ffb386bb70c073216a
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811658"
---
# <a name="page-design-guidelines"></a>ページ デザインのガイドライン

[!include [banner](../../includes/banner.md)]
[!include [mobile app deprecated](../../includes/mobile-app-deprecation-banner.md)]

デザイナーを使用してページとアクションを構築する前に、構築するモバイル ワークスペースの全体的なデザインを計画することが重要です。 モバイル ワークスペースでの使用を予定しているエンティティを中心にして設計の方向を正しく位置付けることをお勧めします。 初めに使用希望のフォームを検討しないでください。 モバイル アプリの観点からは、フォームは単なるデータを取得するためのメカニズムであり、フォームのランタイム UI 動作はモバイル アプリに適用できません。 したがって、エンティティとエンティティ間のリレーションシップを最初に特定する必要があります。 各エンティティについて、以下の質問はフォームやページをどうデザインすべきかを決定するのに役立ちます。

### <a name="how-do-i-create-a-list-view-for-an-entity-in-the-mobile-app"></a>モバイル アプリでエンティティのリスト ビューをどのように作成しますか。

1.  エンティティのグリッドを含む Web クライアントのフォームを識別または作成します。
2.  グリッドがエンティティを表すテーブルにバインドされていることを確認します。
3.  フォームにルート移動可能なメニュー項目があることを確認します。
4.  フォームがメニュー項目のパラメーターを含む URL 経由で直接開くことができることを確認します。
5.  フィルター ウィンドウで、目的のフィールドに基づいてグリッドをフィルター処理できることを確認します。
6.  デザイナーで、エンティティのページを作成します。
7.  デザイナーで、ページ上に一覧のみ配置します。
8.  デザイナーで、一覧にある目的のフィールドをページに配置します。

### <a name="what-if-i-dont-want-a-list-view-for-this-entity"></a>このエンティティの一覧表示が必要ない場合はどうしますか ?

エンティティの詳細ビューだけを使用する場合は、エンティティは、特定のコンテキスト (特定のユーザーや特定の会社など) において単一のエンティティである可能性があります。 このパターンは、たとえば、セルフサービス ワークスペース内の従業員自身のプロファイルの詳細ビューまたは現在のセッションで使用される会社コンテキストの詳細ビューに適用されます。 詳細ビューのページを作成するためのガイドラインを参照してください。

### <a name="how-do-i-create-a-details-view-for-an-entity-in-the-mobile-app"></a>モバイル アプリでエンティティの詳細ビューをどのように作成しますか。

1.  このエンティティの詳細ビューを含む Web クライアントのフォームを識別または作成します。
2.  フォームのマスター ルート データ ソースがエンティティを表すテーブルにバインドされていることを確認します。
3.  フォームにルート移動可能なメニュー項目があることを確認します。
4.  フォームがメニュー項目のパラメーターを含む URL 経由で直接開くことができることを確認します。
5.  デザイナーで、エンティティのページを作成します。
6.  デザイナーで、目的のフィールドをページに配置します。

### <a name="how-do-i-create-list-to-details-navigation-for-an-entity-in-the-mobile-app"></a>モバイル アプリでエンティティ用リストから詳細へのナビゲーションをどのように作成しますか。

1.  デザイナーを使用してエンティティのリスト ビュー ページと詳細ビュー ページの両方を作成したことを確認します。
2.  リスト ビューのエンティティが詳細ビューのエンティティと同じであることを確認します。 つまり、リスト ビューに使用されるフォームのグリッドにバインドされているテーブルは、詳細表示に使用されるフォームでマスター ルート データ ソースとなっている同じテーブルである必要があります。
3.  詳細ビューで使用されるフォームが、フィルター ウィンドウを使用して固有のキー フィールドでフィルターできることを確認します。
4.  デザイナーで、リスト ビュー ページが詳細表示ページにリンクされていることを確認します。 リストをクリックしてプロパティを開き、ルックアップを使用して詳細表示ページを設定します。 

    ![リスト ビュー ページを詳細ビュー ページにリンクします。](media/listtodetailsdesigner.png)

### <a name="how-do-i-add-a-reference-field-that-enables-navigation-to-a-related-entity"></a>ナビゲーションを有効にする参照フィールドを関連するエンティティに追加する方法はありますか。

1.  参照を含むエンティティに対して、リスト ビュー ページまたは詳細ビュー ページのいずれかが存在することを確認します。
2.  ページに参照されているエンティティから参照フィールドが含まれていることを確認します。
3.  参照先のフィールドが参照先のエンティティのデータ ソースにバインドされており、参照先のエンティティが参照を含むエンティティのデータ ソースに *外部結合*(1-0..1) または *内部結合*(1-1) されていることを確認します。 たとえば、次の図では、FMRental は参照を含むエンティティで、FMVehicle は参照されたエンティティです。

    ![参照フィールドを参照されるエンティティのデータ ソースにバインドします。](media/relatedentityform.png)

4.  参照されているエンティティに対して個別の詳細ビュー ページを作成したことを確認します。
5.  参照フィールドがページに追加されたことを確認します。
6.  デザイナーで、参照フィールドが参照されているエンティティの詳細表示にリンクされていることを確認します。 たとえば、次の図では、車両詳細は参照されたエンティティの詳細ビュー ページです。

     ![参照フィールドを、参照先エンティティの詳細ビューにリンクします。](media/referencepagedesigner.png)

### <a name="how-do-i-add-a-list-that-contains-items-from-a-related-entity-to-a-details-view-page"></a>関連するエンティティからの品目を含む一覧を、詳細ビュー ページに追加する方法はありますか。

###### <a name="how-do-i-make-the-list-show-up-in-line-in-the-details-view"></a>詳細ビューでインラインを表示できるようするにはどうすればよいですか。

1.  エンティティの詳細ビューを含む Web クライアントのフォームを識別または作成し、フォームが「モバイル アプリケーションのエンティティの詳細ビューを作成する方法」のガイドラインに従っていることを確認します。
2.  フォームが関連するエンティティを表すテーブルにバインドされているグリッドを含むことを確認します。
3.  関連するエンティティのテーブルが参照を含むエンティティのテーブルに *アクティブに結合* されていることを確認します。
4.  エンティティの目的のフィールドを含む詳細ビュー ページを作成します。また、関連エンティティの希望のフィールドを持つリストも含まれます。

###### <a name="how-do-i-make-the-list-accessible-from-a-link-in-the-details-view-instead-of-in-line"></a>詳細ビュー (インラインではなく) のリンクからリストにアクセスできるようするにはどうすればよいですか。

1.  エンティティの詳細ビューを含む Web クライアントのフォームを識別または作成し、フォームが「モバイル アプリケーションのエンティティの詳細ビューを作成する方法」のガイドラインに従っていることを確認します。
2.  フォームが関連するエンティティを表すテーブルにバインドされているグリッドを含むことを確認します。
3.  関連するエンティティのテーブルが参照を含むエンティティのテーブルに *アクティブに結合* されていることを確認します。
4.  フォームを使用して、エンティティの目的のフィールドを含む詳細ビュー ページを作成します。
5.  同じフォームを使用して、関連するエンティティから目的のフィールドを持つリストのみを含む別のリスト ビュー ページを作成します。
6.  詳細表示ページで、リスト表示ページにリンクする PageLinkControl を追加します。 現在、ビジネス ロジックを使用して PageLinkControl を追加する必要があります。 次の例は、Fleet Management が使用するコードを示しています。

    ```xpp
    function main(metadataService, dataService, cacheService, $q) { 
        return { 
            appInit: function (appMetadata) { 
                metadataService.addLink( 
                    'Customer-details', // the Page to add the link to 
                    'Customer-rentals', // the Page the link goes to 
                    'cust-rentals-nav-control', // unique name for the control 
                    'Rentals', // text to display for the link in the UI 
                    true, // show/hide the count for items on the linked page 
                    ); 
            }, 
        }; 
    }
    ```

###### <a name="how-do-i-read-data-from-a-hidden-page"></a>非表示ページからデータを読み取るにはどうすればよいですか。

1.  希望するデータでコントロールを含むページを識別または作成します。
2.  次のコード例をご覧ください。ナビゲーション メニューからページを非表示にし、提供される API を使用してページ上のデータにアクセスします。 「My-Hidden-Page」および「My-Field-Id」は、それぞれページおよびコントロールの名前であり、デザイナーで対応するページを表示するときに確認できることに注意してください。

    ```xpp
    function main(metadataService, dataService, cacheService, $q) {
        myField1Value = ''; // This variable will be populated in appInit, and can then be used elsewhere in the business logic. 
        return { 
            appInit: function (appMetadata) { 
                var myHiddenPage = metadataService.findPage('My-Hidden-Page');
                if(myHiddenPage) {
                    var dataPromise = dataService.getPageData(myHiddenPage.Id,'','',0);
                    dataPromise.then(function (result) {
                        var myField1Id = metadataService.findControl(myHiddenPage, 'My-Field-1').Id;
                        myField1Value = result.data[myField1Id];
                    }
                }
        }; 
    }
    ```

### <a name="how-do-i-adjust-the-number-of-records-returned-in-a-list-page-using-list-fetch-size"></a>リスト フェッチ サイズを使用して、リスト ページで返されるレコードの数を調整する方法はありますか。

リストページで返されるレコードの数は、**List fetch size** 値によって制御されます。 既定は 50 レコードです。 **リスト フェッチ サイズ** は、最初に読み込まれたときにページにより返されたレコードの最大数と、検索を使用して特定のレコード セットが検索されたときに返されたレコードの最大数を示します。 値を大きくしすぎないように注意が必要です。ユーザー エクスペリエンスに悪影響を与える可能性があります。

1. モバイル アプリ デザイナーで、グリッドを含むページを追加し、グリッドからいくつかのフィールドを選択します。
2. **グリッド** ノードをクリックし、**プロパティ** をクリックします。
3. **コントロールのプロパティ** ダイアログ ボックスには 50 件のレコードの既定のフェッチ サイズが表示されます。
4. 必要に応じて、フェッチ サイズを調整します。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

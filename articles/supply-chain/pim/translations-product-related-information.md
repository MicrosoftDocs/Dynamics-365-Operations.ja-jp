---
title: 製品関連の翻訳のよく寄せられる質問
description: この記事では、製品の翻訳、製品分析コードの値、および製品属性を管理する方法について説明します。
author: t-benebo
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList, EcoResProductListPage, EcoResProductVariants, EcoResProductDetailsExtended, EcoResProductCreate, EcoResProductDetails, RetailSizeGroupTable, RetailStyleGroupTable, RetailColorGroupTable, PCTranslationLanguageLookup, EcoResProductCategory
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 079e6de00d1a946d998648378d5ca24c1fd26218
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015409"
---
# <a name="product-related-translations-faq"></a>製品関連の翻訳のよく寄せられる質問

[!include [banner](../includes/banner.md)]

この記事では、製品の翻訳、製品分析コードの値、および製品属性を管理する方法について説明します。 

## <a name="what-product-related-data-can-be-translated"></a>どの製品関連データは翻訳できますか。

次の製品関連情報の翻訳を作成できます。
-   製品の名前と説明。
-   製品属性値の説明、フレンドリ名、およびヘルプ テキスト。
-   製品分析コード値の名前と説明。

**テキストの翻訳** ページから使用できる任意の言語に、製品関連情報を翻訳できます。 詳細については、**製品関連情報の翻訳を作成する方法** を参照してください。

## <a name="where-can-i-view-the-translated-information"></a>翻訳された情報はどこで表示できますか。
製品関連情報の翻訳は、翻訳で利用可能な言語を使用する、請求書などの外部元伝票すべてで表示できます。

## <a name="how-do-i-create-translations-for-product-related-information"></a>製品関連情報の翻訳を作成する方法。
製品の翻訳を作成するには、次の手順に従います。
1.  **製品情報管理** &gt; **製品** &gt; **リリースされた製品** の順にクリックします。
2.  製品を選択して、[アクション ペイン] の、**言語** グループで **翻訳** をクリックします。
3.  **テキストの翻訳** ページの **言語** フィールドで、言語を選択します。 さらに言語を追加するには、**言語** フィールドを展開してから **OK** をクリックします。
4.  **翻訳テキスト** グループの、**説明** および **製品名** フィールドに翻訳を入力します。

製品属性の翻訳を作成するには、次の手順に従います。
1.  **製品情報管理** &gt; **製品** &gt; **リリースされた製品** の順にクリックします。
2.  **設定** で、**属性** をクリックし、**属性** をクリックします。
3.  **属性** ページで、**翻訳** をクリックします。
4.  **テキストの翻訳** ページの **言語** フィールドで、言語を選択します。 さらに言語を追加するには、**言語** フィールドを展開してから **OK** をクリックします。
5.  **翻訳テキスト** グループの、**説明**、**フレンドリ名**、および **ヘルプ テキスト** フィールドに翻訳を入力します。

製品分析コードの値の翻訳を作成するには、次の手順に従います。
1.  **製品情報管理** &gt; **製品** &gt; **リリースされた製品** の順にクリックします。
2.  製品を選択してから、**製品分析コード** をクリックします。
3.  製品分析コードへのリンク、**コンフィギュレーション**、**サイズ**、**色**、または **スタイル** のいずれかを選択します。
4.  分析コードの値を選択し、**翻訳** をクリックします。
5.  **テキストの翻訳** ページの **言語** フィールドで、言語を選択します。 さらに言語を追加するには、**言語** フィールドを展開してから **OK** をクリックします。
6.  **翻訳テキスト** グループで、**名前** および **説明** フィールドに翻訳を入力します。

## <a name="can-the-names-of-product-variants-be-translated"></a>製品バリアントの名は翻訳できますか。
製品バリアントは、リリース済み製品の分析コードに基づきます。 製品バリアントの名前は、分析コードの値の組み合わせに基づきます。 製品バリアントに関連付けられている分析コード値が翻訳されると、製品バリアントの名前は翻訳済みのバージョンに表示されます。  

**例**  

ユーザーの製品は T シャツで、異なるサイズと色があり、バリアント名は以下の詳細に基づきます。
-   製品番号: \#3
-   分析コード: サイズおよび色
-   サイズ分析コードの値: S、M、L
-   カラー分析コードの値: 赤、緑、黒

分析コードの値 S と赤に基づく製品バリアントの名前は **\#3:S: 赤** です。  

ある顧客は S で赤い T シャツを購入したいと思い、T シャツの名前は請求書にフランス語で表示する必要があります。 分析コードの値、S および赤をフランス語に翻訳すると、製品バリアント名は **\#3:Petit:Rouge** となります。
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>ヒント</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>顧客が希望する言語を設定するには、次の手順に従います。
<ol><br/><li><strong>販売およびマーケティング</strong> &gt; <strong>共通</strong> &gt; <strong>顧客</strong> &gt; <strong>すべての</strong> <strong>顧客</strong> をクリックします。</li>
<li>顧客をダブルクリックして、<strong>顧客</strong> ページを開きます。 <strong>一般</strong> タブの <strong>言語</strong> フィールドで、<strong>言語</strong> を選択します。</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>顧客の希望する言語では翻訳を利用できない場合はどうしますか。
顧客の希望する言語では翻訳が使用できない場合、名前と説明はユーザーの会社の国際語で表示されます。

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>一連の分析コード値の翻訳は同時に管理できますか。
分析コード値は製品固有であり、製品ごとに分析コード値の翻訳を管理できます。 ただし、分析コード値のグループを作成し、値グループで値の翻訳を作成するなら、翻訳の管理が容易になります。   

**例**  

ユーザーの会社の製品である T シャツには異なるスタイルがあり、どのスタイルでも S、M、L を利用できます。 サイズは、1 種類の分析コード値のグループに収集されます。 新しい T シャツのスタイルが追加されると、すべてのサイズが製品で使用できるように、サイズに使用される分析コード値のグループと関連付けることができます。 サイズの翻訳は、分析コード値グループで同時に追加または変更できます。  

分析コードのさまざまなグループを使用して製品に関連付けられている分析コード値は、製品バリアント グループから管理する必要があります。   
分析コード値グループを作成するには、次の手順に従います。
1.  **製品情報管理** &gt; **設定** &gt; **バリアント グループ** の順にクリックします。
2.  **サイズ** **グループ**、**色グループ** または **スタイル グループ** を選択します。
3.  **新規** をクリックし、**サイズ** **グループ**、**色グループ**、または **スタイル グループ** フィールドにグループの名前を入力します。 **サイズ**、**色** または **スタイル** をクリックして、グループの明細行を作成します。
4.  **サイズ** **グループ** 明細行、**色** **グループ** **明細行**、または **スタイル グループ明細行** ページで、**新規** をクリックし、グループのためにサイズ、色、およびスタイルを作成します。

分析コード値グループの値の翻訳を管理するには、次の手順を実行します。
1.  分析コード値グループを作成するための以前の手順に従い、**サイズ グループ明細行**、**色グループ明細行** または **スタイル グループ明細行** ページを開くます。
2.  **テキストの翻訳** をクリックします。 **テキストの翻訳** ページの **翻訳テキスト** グループで、**名前** および **説明** フィールドに翻訳を入力します。

## <a name="when-can-translations-of-product-related-information-be-managed"></a>製品関連情報の翻訳はいつ管理できますか。
製品関連情報の翻訳はいつでも管理できます。 製品と関連付けられている分析コード値の翻訳が更新されると、製品に翻訳があるかどうかに関係なく、製品情報が更新されます。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
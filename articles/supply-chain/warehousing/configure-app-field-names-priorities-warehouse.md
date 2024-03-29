---
title: Warehouse Management モバイル アプリのフィールドを構成する
description: この記事では、倉庫管理モバイル アプリのフィールド名と優先順位の定義および構成方法について説明します。
author: Mirzaab
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 00a20faaa05a9d0891ee202951b1ca50d0176c83
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065961"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a>Warehouse Management モバイル アプリのフィールドを構成する

[!include [banner](../includes/banner.md)]

この記事では、倉庫管理モバイル アプリのフィールド名と優先順位の定義および構成方法について説明します。

> [!NOTE]
> この記事は、倉庫管理の機能に適用されます。 在庫管理の機能には適用しません。 倉庫管理モバイル アプリは、倉庫タスクの実行に使用できるアプリケーションです。 アプリで使用されるフィールド名を定義してコンフィギュレーションし、フィールド名に割り当てる優先順位をフィールド名をコンフィギュレーションできます。 この記事では、これらの倉庫管理モバイル アプリのフィールド名と優先順位の定義および構成方法と使用方法について説明します。

## <a name="configure-warehouse-app-field-names"></a>倉庫アプリ フィールド名のコンフィギュレーション

Warehousing をモバイル デバイスで使用するときに、**倉庫アプリ フィールド名** ページでお使いのデバイスにメタデータをどのように表示するかをコンフィギュレーションできます。 新しい会社で、**既定の設定の作成** をクリックして倉庫モバイル デバイス ワークフローで使用されるすべてのフィールド名を生成してから、優先される入力モードと入力タイプを割り当てます。 すべてのフィールド名を生成すると、次の入力オプションを選択できます。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>オプション</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>優先入力モード</td>
<td>このオプションは、スキャン フィールドまたは手動入力フィールドを選択したフィールド名に表示するかどうかを定義します。 これは、バーコードがフィールドに使用されるかどうかによって、フィールドを区別する場合に役立ちます。 <strong>注記: </strong> 優先入力モードを<strong>スキャン</strong>に設定したフィールド名では、バーコードが読み取れない場合や破損している場合に手動で情報を入力できます。</td>
</tr>
<tr class="even">
<td>入力タイプ</td>
<td>このオプションは、どの入力タイプを選択したフィールド名に使用するかを定義します。 次の 4 つのオプションが使用可能です。
<ul>
<li><strong>選択</strong> - 選択するオプションの一覧を含みます。 このオプションのフィールド名は編集できません。</li>
<li><strong>日付</strong> - 日付として指定されたフィールド名がラベルとともに日付形式で表示されます。 これは、倉庫作業者が日付を入力する形式を確認するのに役立ちます。 このオプションのフィールド名は編集できません。</li>
<li><strong>アルファ</strong> - 選択されている場合、アプリに手動で情報を入力する際にデバイス キーボードを使用します。 使用するデバイスに応じて、キーボード エクスペリエンスを変更することができます。</li>
<li><strong>数値</strong> - 数値入力のみを使用するフィールド名では、このオプションを選択してデバイス キーボードではなくカスタムのテンキーを入力フィールドとともに表示できます。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>倉庫アプリ フィールドの優先順位のコンフィギュレーション

**倉庫アプリ フィールドの優先順位** ページで、フィールド名を異なる優先順位グループに配置できます。 これにより、倉庫作業者がアプリを使用してタスクを実行する際に、どの情報を主要なタスク ページに表示すべきかを決定することができます。 **既定の設定の作成** をクリックすると、優先順位グループの既定の設定が生成されます。 必要な数だけ優先順位グループを作成することもできますが、3 つの優先順位グループだけがタスク ページに表示されます。 システムはアプリにメタデータを送信する際に、優先順位グループに応じて各フィールドに相対的な優先順位を割り当てて、アプリはメタデータを含む上位 3 つの優先順位グループをタスク ページに表示します。 オーバーフローしているメタデータの残りは、2 番目の詳細ページに表示されます。 次の表に、5 つの優先順位グループの例を示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>優先順位グループ</th>
<th>割り当て済フィールド</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> 優先順位 10</td>
<td><ul>
<li>項目</li>
<li>件数</li>
<li>計量単位</li>
</ul></td>
</tr>
<tr class="even">
<td> 優先順位 20</td>
<td><ul>
<li>クラスター位置</li>
<li>クラスター</li>
</ul></td>
</tr>
<tr class="odd">
<td> 優先順位 30</td>
<td><ul>
<li>品目の説明</li>
</ul></td>
</tr>
<tr class="even">
<td> 優先順位 40</td>
<td><ul>
<li>構成</li>
<li>色</li>
<li>サイズ</li>
<li>スタイル</li>
</ul></td>
</tr>
<tr class="odd">
<td> 優先順位 50</td>
<td><ul>
<li>保管場所</li>
<li>ライセンス プレート</li>
</ul></td>
</tr>
</tbody>
</table>

たとえば、倉庫作業者がモバイル デバイスのタスクを実行しているときに、アプリケーションに表示されるメタデータが次のフィールドで構成されている場合 :

-   項目
-   件数
-   計量単位
-   品目の説明
-   サイズと場所

上の表で設定されている倉庫アプリ フィールドの優先順位に基づいて、情報の次の 3 行は、タスク ページに表示されます :

-   行 1: 品目、数量、測定単位
-   行 2: 品目の説明
-   行 3 : サイズ

場所などの残りのメタデータは、タスク ページに表示されませんが、詳細ページに表示されます。 ユーザー インターフェイスの詳細や例については、ブログ投稿 [Dynamics 365 Supply Chain Management - Warehousing の発表](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/) を参照してください。

## <a name="additional-resources"></a>追加リソース

[倉庫管理モバイル アプリのインストールと接続](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

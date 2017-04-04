---
title: "アプリケーションの倉庫のアプリケーションのフィールド名を設定します。"
description: "このトピックでは、Dynamics 365 for Operationsの倉庫のアプリケーションのフィールド名と優先順位を定義およびコンフィギュレーション方法について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>アプリケーションの倉庫のアプリケーションのフィールド名を設定します。

このトピックでは、Dynamics 365 for Operationsの倉庫のアプリケーションのフィールド名と優先順位を定義およびコンフィギュレーション方法について説明します。 

**注記: **このトピックでは、倉庫管理機能に適用されます。 [在庫管理機能には適用されません。 Dynamics 365 for Operationsの倉庫が倉庫作業を実行で使用できるアプリケーションです。 定義し、アプリケーションをコンフィギュレーションして使用される、フィールド名を割り当てる優先順位をフィールド名を設定できます。 このトピックでは、これらの倉庫のアプリケーションのフィールド名と優先順位を定義およびコンフィギュレーション方法を説明し-方法に、Dynamics 365 for Operationsで使用されている倉庫します。 保管するDynamics 365 for Operationsへの接続を]保管して、個人ガイダンスを参照して、[Dynamics 365 for Operationsをインストールしてコンフィギュレーションします] -設定する方法についての詳細 (倉庫を設定しますapp.md)。

<a name="configure-warehouse-app-field-names"></a>倉庫のアプリケーションのフィールド名を設定します。
===================================

Dynamics 365 for Operationsのメタデータのデバイスに表示するかを設定して、[モバイル デバイスで倉庫は**倉庫はアプリケーションのフィールド名**ページを使用する場合)。 [Dynamics 365 for Operationsの新しい会社で**既定の設定を作成します。**倉庫のモバイル デバイスの現在の作業で使用されるすべてのフィールド名を生成すると、それに、推奨入力モード、[入力タイプを割り当てる。 すべてのフィールド名を生成した後、オプションを送信するには、以下を選択できます。

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
<td>このオプションは、スキャン フィールドまたは手動による入力の入力]フィールドで選択したフィールドの名前に表示するかどうかを定義します。 これは、バーコード]フィールドに使用されるフィールドで指定する場合に役立ちます。 <strong>注:</strong> に設定されている優先入力モードのフィールド名のバーコードが不可能判読または傷つけられる情報を手動で入力できます。</td>
</tr>
<tr class="even">
<td>入力タイプ</td>
<td>このオプションは、[入力タイプが選択したフィールドの名前に使用する方法を定義します。 4つのオプションを使用できます:
<ul>
<li><strong>選択</strong> - 選択するオプションを示します。 このオプションのフィールド名は編集できません。</li>
<li><strong>日付</strong>日付として指定した - フィールド名はラベルでの日付の形式を示します。 これは、日付を入力するか、フォームの倉庫作業員の情報を表示する。 このオプションのフィールド名は編集できません。</li>
<li><strong>この</strong>選択されている場合、デバイスの -、情報をアプリケーションに手動で入力するときに使用されます。 デバイスを使用するキーボード エクスペリエンスを変更することができます。</li>
<li><strong>数値</strong>数値入力のみを使用するフィールド名 -、デバイスのではなく入力フィールドを含むカスタム数値キーパッドを表示する場合は、このオプションを選択できます。</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>倉庫のアプリケーション フィールド優先順位を設定します。
======================================

**アプリケーション フィールド優先順位を倉庫。**ページで、異なる優先順位グループのフィールド名を送信します。 これは、倉庫作業員がアプリケーションを使用してタスクを実行すると、情報が主要なタスク ページに表示するかを決定することができます。 **既定の設定を作成します。**クリックすると、優先順位グループの既定の設定が生成されます。 必要な数だけ優先順位グループを作成することもできますが3つの優先順位グループはタスク ページに表示されます。 Dynamics 365 for Operationsは、アプリケーションにメタデータを送信する場合は、優先順位グループ別に各フィールドの相対的な優先順位を割り当て、タスク ページのメタデータに含まれている最初の3つの優先順位グループを表示します。 キャッシュ アウトフローのメタデータの他に二次詳細ページに表示されます。 次の表に、5つの優先順位グループの例を示します。

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
<td> 優先順位10</td>
<td><ul>
<li>項目</li>
<li>件数</li>
<li>計量単位</li>
</ul></td>
</tr>
<tr class="even">
<td> 優先順位20</td>
<td><ul>
<li>クラスター位置</li>
<li>クラスター</li>
</ul></td>
</tr>
<tr class="odd">
<td> 優先順位30</td>
<td><ul>
<li>品目の説明</li>
</ul></td>
</tr>
<tr class="even">
<td> 優先順位40</td>
<td><ul>
<li>構成</li>
<li>色</li>
<li>サイズ</li>
<li>スタイル</li>
</ul></td>
</tr>
<tr class="odd">
<td> 優先順位50</td>
<td><ul>
<li>保管場所</li>
<li>ライセンス プレート</li>
</ul></td>
</tr>
</tbody>
</table>

たとえば、倉庫作業員がモバイル デバイスのタスクを実行すると、アプリケーションに表示されるメタデータが次のフィールドから構成されている場合:

-   項目
-   件数
-   計量単位
-   品目の説明
-   サイズと場所

上の表で設定されている倉庫のアプリケーション フィールド優先順位に基づいて情報の次の3つの行は、タスク ページに表示されます:

-   行1: 品目、数量を選択
-   行2: 品目の説明
-   行3: サイズ

残りのメタデータなどのタスク ページに表示されませんが、詳細ページに表示されます。 多くの情報と、ユーザー インターフェイスの例を表示するには、ブログの転記を参照して、[Dynamics 365 for Operationsをリリースする-倉庫は] (https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)。

<a name="see-also"></a>参照
--------

[保管する工程は–のMicrosoft Dynamics 365をインストールしてコンフィギュレーションします] (倉庫を設定しますapp.md) 



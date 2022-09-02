---
title: USER INPUT PARAMETER データ ソースを使用してレポートのパラメータを指定する
description: この記事では、ユーザー入力パラメータデータ ソースを使用して、生成するレポートのパラメータを指定する方法について説明します。
author: kfend
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: c6d0f1a0d9c5eb70a9812459a25d5b14407cce7a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278710"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>USER INPUT PARAMETER データ ソースを使用してレポートのパラメータを指定する

[!include[banner](../includes/banner.md)]

[電子レポート](general-electronic-reporting.md) (ER) [モデル マッピング](er-overview-components.md#model-mapping-component) と ER [形式](er-overview-components.md#format-component) コンポーネントをデザインする場合、ER フォーマットの開始の実行前に *USER INPUT PARAMETER* タイプのデータ ソースを使用して実行時にデータ入力フィールドで指定できる必須の値を取得できます。 この記事では、現在サポート されている *USER INPUT PARAMETER* データ ソースについて説明します。

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>必須プロパティ

各 *USER INPUT PARAMETER* タイプのデータ ソースには、次のプロパティを指定する必要があります。

- **名前** フィールドに、データ ソースの名前を入力します。 この名前は、他の [式](er-formula-language.md) と、構成されたモデル マッピングまたは書式設定コンポーネントのバインドで使用できます。

## <a name="optional-properties"></a><a name="optional-properties"></a>オプションのプロパティ

*USER INPUT PARAMETER* タイプのデータ ソースには、次のプロパティをオプションで指定できます。

- **ラベル** フィールドで、実行時のダイアログ ボックスの関連するデータ入力フィールドに使用されるラベルを指定します。 異なる言語コードに対して異なるラベル テキストを追加するには **ラベル** フィールドを有効化し、**翻訳** を選択します。
- **ヘルプ** フィールドで、*USER INPUT PARAMETER* タイプの編集可能なデータ ソースを選択するときに、**形式デザイナー** ページまたは **モデル マッピング デザイナー** ページの下にデザイン時に表示されるヘルプ テキストを指定します。 このテキストは、ユーザーが編集可能な形式またはモデル マッピング コンポーネントを構成する際に役立つデータ ソースに関する追加情報を提供する場合があります。 **翻訳** を選択すると、異なる言語コードに対して異なるヘルプ テキストを追加できます。

    > [!NOTE]
    > [言語固有のラベルとテキスト](er-design-multilingual-reports.md#format-component) を追加するために使用できる **翻訳** ボタンは、データ ソースを追加し、変更を保存し、編集用にデータ ソースを再度開いた後にのみ使用できます。

- **読み取り専用** フィールドで、*[ブール](er-formula-supported-data-types-primitive.md#boolean)* 値を返す式を構成します。

    - 実行時に、構成済みの式で値が **True** を返す場合、関連するデータ入力フィールドはダイアログ ボックスに表示され、値を変更することはできません。
    - 実行時に、構成済みの式で値が **False** を返す場合、または式が構成されていない場合、関連するデータ入力フィールドはダイアログ ボックスにあり、値を変更することはできません。

- **既定値** フィールドで、参照するパラメータ タイプの値を返す式を構成します。 この値を使用して、実行時のダイアログ ボックスで関連するデータ入力フィールドの既定値を入力できます。

    ER 形式を実行すると、実行時にダイアログ ボックスの関連データ入力フィールドに入力した値が、以前に使用した値としてメモリに保存されます。 以前に使用した値は、ER 形式、現在のユーザー、および現在の組織 (会社) を実行して、フィールドごとに個別に保存されます。

    - 以前に使用した値に関係なく、**既定値** の式で返される値を常に既定値として使用する必要がある場合は、**常に既定値にリセットする** オプションを **はい** に設定します。
    - **既定値** の式で返される値を以前に使用した値がない場合のみ規定値として使用する必要がある場合は、**常に既定値にリセットする** オプションを **いいえ** に設定します。

    > [!NOTE]
    > **常時既定値にリセット** オプションを **はい** に設定した場合、**既定値** フィールドで式を構成する必要があります。

- **複数選択を許可する** オプション を **はい** に設定 した場合は、実行時に構成されたパラメータに対して複数の値を選択できます。 **いいえ** に設定 した場合、1 つの値のみを選択できます。

    > [!NOTE]
    > このオプションは、すべての *USER INPUT PARAMETER* タイプには適用できません。 設計時には、構成済みのユーザー入力パラメータが複数の選択をサポートしなく、1 つの値のみを選択または入力できるような例外がユーザーに通知されます。
    >
    > **複数選択を許可する** オプションを **はい** に設定し、**既定値** フィールドで式を指定した場合、その式を使用して 1 つの既定値のみを設定できます。

- **可視性の編集** オプションを選択して、実行時にダイアログ ボックスに構成済パラメータを表示するかどうかを指定します。

    > [!NOTE]
    > *USER INPUT PARAMETER* タイプのデータ ソースの既定の可視性は、それらを保持する ER コンポーネントによって異なります。
    >
    > - データ ソースが形式コンポーネントで構成されている場合は、既定でデータ ソースが表示されます。
    > - モデル マッピング コンポーネントでデータ ソースが構成されている場合、そのデータ ソースの値が ER コンポーネントの実行時の結果に影響する場合にのみ表示されます。 たとえば、データ ソースを追加したが、データ ソースは、現在のモデル マッピング コンポーネントの式とバインドでは使用されません。 この場合、既定では、関連するデータ入力フィールドは実行時のダイアログ ボックスに表示されません。 

    **フォーミュラ デザイナー** ページの **式** フィールドで、*ブール* 値を返す式を構成します。

    - 実行時に、構成済みの式で値が **True** を返す場合、または式が構成されていない場合、関連するデータ入力フィールドは実行時にダイアログ ボックスに表示されます。
    - 構成済式が **False** の値を返す場合、実行時のダイアログ ボックスには関連するデータ入力フィールドは表示されません。 実行時に他の式によって呼び出された場合は、その他の設定に応じて、既定値、以前に使用した値、または現在のデータ型の値の既定値を返します。

## <a name="type-specific-properties"></a>タイプ指定型のプロパティ

### <a name="application-dependent-user-input-parameter"></a>アプリケーション依存のユーザー入力パラメータ

**一般** \> **ユーザー入力パラメータ** タイプのデータ ソースを使用して、Microsoft Dynamics 365 Finance アプリケーションの現在のインスタンスに対して指定されているデータ型の必要な値または値を取得します。 このタイプのデータ ソースをERコンポーネントに追加する場合は、次のプロパティを指定します。

- **操作データ型名 (EDT, enum)** フィールドで、アプリケーション [拡張データ型 (EDT)](../extensibility/extensible-edts.md) またはアプリケーションの変更に使用するアプリケーションを選択します。

> [!NOTE]
> この *USER INPUT PARAMETER* タイプの編集可能なデータ ソース内で **操作データ型名 (EDT, enum)** 参照を変更する際には、**読み取り専用** フィールドおよび **既定値** フィールドで構成されている式を確認することをお勧めします。

次の図は、**Instat XML (DE)** ER 形式構成で構成された`$TaxRegNum` データ ソースのプロパティを示しています。 このデータ ソースは、*説明 EDT* を使用して、実行時にダイアログ ボックスで **税登録番号** データ入力フィールドを提供するように構成されます。

![ユーザー入力パラメータのデータ ソースのプロパティは、形式デザイナー ページのダイアログ ボックスを入力します。](./media/er-user-input-parameter-data-sources-01.png)

次の図は、イントラスタット申告を [生成](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) するために **Instat XML (DE)** ER 形式構成を実行するときに実行時に表示されるダイアログ ボックスを示します。 構成済の **税登録番号** フィールドが データ入力に使用できるのに注意してください。

![イントラスタット ページで実行されている ER 形式のイントラスタット レポート ダイアログ ボックス。](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>データ モデル列挙ユーザー入力パラメーター

**データ モデル** \> **リスト ユーザー入力パラメータ** タイプのデータ ソースを使用して、単一のデータ モデル [リスト](er-formula-supported-data-types-primitive.md#enumeration) から求められる値を取得します。 このタイプのデータ ソースをERコンポーネントに追加する場合は、次のプロパティを指定します。

- **モデル** フィールドで、基本データ モデルへの参照を指定します。
- **モデルリスト** フィールドで、参照するデータ モデルのリストへの参照を指定します。
- [バージョン] **フィールド** で、参照モデルの変更を含むERデータ モデル コンポーネントのリビジョン番号を選択します。

    > [!TIP]
    > デザイン時には、**バージョン** フィールドを空白のままにして、対応する ER データ モデル構成のドラフト バージョンに存在する参照データ モデル コンポーネントの選択項目の一覧にアクセスできます。 これにより、モデル のマッピングまたは書式設定コンポーネントのドラフト バージョンと、基本データ モデル コンポーネントのドラフト バージョンを同時に編集できます。
    >
    > ただし、**バージョン** フィールド は、モデル マッピングまたは形式コンポーネントのドラフト バージョンでのみ空白のままにすることができます。 ER モデルのマッピングまたは形式の構成のステータスを **ドラフト** から **完了** に変更すると、このフィールドには、現在の財務インスタンスで使用できる最高のモデルリビジョン番号が自動的に入力されます。 基本データ モデルのドラフト バージョンで新しいオブジェクト名を指定する場合、または、その値を編集可能なモデル マッピングまたは形式コンポーネントで参照する場合は、ER モデルのマッピングまたは形式の構成のドラフト バージョンを完了する前に、基本データ モデル構成のドラフト バージョンを作成します。 そうでない場合は、モデル のマッピングまたは形式の構成のステータスを **ドラフト** から **完了** に変更すると、"パスが見つかりません" という例外が表示されます。 このメッセージは、基本データ モデルに参照しているオブジェクト名またはオブジェクト名の値が存在しなくてすむという通知を表示します。

次の図は、**Instat XML (DE) Contoso** ER 形式構成で構成された`$ReportDirection` データ ソースのプロパティを示しています。 **Instat XML (DE) Contoso** 構成は、**Instat XML (DE)** 構成から [派生](general-electronic-reporting.md#Configuration) しています。 このデータ ソースは、*ReportDirection* モデル リストを使用して、実行時にダイアログ ボックスで適切な検索フィールドを提供するように構成されます。

![形式デザイナー ページのダイアログ ボックスの USER INPUT PARAMETER タイプのデータ ソースのプロパティ。](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>形式列挙ユーザー入力パラメーター

**形式リスト** \> **リスト ユーザー入力パラメータ** タイプのデータ ソースを使用して、単一の形式リスト から求められる値を取得します。 このタイプのデータ ソースをERコンポーネントに追加する場合は、次のプロパティを指定します。

- **形式リスト** フィールドでは、編集可能な形式の適用方法を指定します。

> [!NOTE]
> このタイプのデータ ソースは、編集可能な形式コンポーネントの範囲でのみ構成できます。

## <a name="additional-resources"></a>追加リソース

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[USER INPUT PARAMETER タイプのデータ ソース値をソース コードから開始する](er-initiate-uip-data-source-value-from-source-code.md)
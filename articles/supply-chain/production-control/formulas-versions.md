---
title: フォーミュラとフォーミュラ バージョン
description: この記事では、フォーミュラとフォーミュラ バージョンについて説明します。 フォーミュラは材料、成分、およびプロセス製造での特定プロセスの結果を定義します。 フォーミュラは、プロセス製造で製品を計画および生産するのに使用されます。
author: johanhoffmann
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule, EcoResProductProdTypeFormulaNoActiveFormulaFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 236a283736078e80506a1ecaab53c013a91c3721
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844151"
---
# <a name="formulas-and-formula-versions"></a>フォーミュラとフォーミュラ バージョン

[!include [banner](../includes/banner.md)]

フォーミュラは材料、成分、およびプロセス製造での特定プロセスの結果を定義します。 対応する工順と共に、フォーミュラはプロセス製造での全体のプロセスを定義します。 フォーミュラは、プロセス製造で製品を計画および生産するのに使用されます。

フォーミュラは、構成要素およびフォーミュラ品目の特定の数量を生産するのに必要な数量で構成されます。 実行するタスクによって、[在庫および倉庫管理] または [製品情報管理] から式機能にアクセスできます。

## <a name="formulas-and-formula-lines"></a>式と式明細行
式は 1 つ以上の式明細行で構成され、この明細行は、式を構成する材料または品目を識別します。 式明細行には部品表 (BOM) 品目、式品目、Catch Weight 品目、購買品目、連産品、副産物が含まれる可能性があります。 多くの品目が複数の製品で使用されるので、1 つの品目を複数のフォーミュラで使用できます。

式の例では、チョコ チップ クッキーの式です。 この式の材料は、小麦粉、砂糖、卵、バター、チョコ チップなどの複数の明細行を使用します。 チョコ チップ クッキーの式には他の式で使用される材料が含まれます。 チョコ チップ クッキーの作成中に、少量の残りものがある可能性があり、一部のクッキーが焼かれたか焼いている途中の可能性があります。 これらの品目は、生産の工程で連産品または副産物として設定できます。

式明細行を作成する場合、マスター プランを実行しバッチ オーダーを生産する際にどのようにシステムを処理すべきかを指定する明細行タイプを使用します。 選択した明細行タイプに応じて結果が異なります。 次の表では、選択できる行タイプについて説明します。 

| 行タイプ     | 説明  |
|---------------|--------------|
| 項目          | 品目が在庫からピッキングされる原材料または半完成品目である場合、または品目がサービスである場合は、**品目** を選択します。 |
| ファントム       | 式明細行に含まれる下位レベルの式品目をすべて展開する場合は、**ファントム** を選択します。 バッチ オーダーを見積もり、式品目が配置されると、コンポーネント品目はバッチ オーダーの式明細行として表示されます。 また、対応する工順が生産工順に追加されます。 式品目は、現在のコンフィギュレーションを使用して展開されます。 **ファントム** 細行タイプを使用すると、異なる式レベルで発生する生産および測定コンフィギュレーションを処理できます。 **ファントム** を **リリース済製品の詳細** ページの **エンジニア** クイック タブ上の製品に選択し、この製品を式で使用する場合、式明細行の明細行タイプは **ファントム** に変更されます。 CW 品目、または製品タイプが **連産品**、**副産物**、または **計画品目** の品目に対して **ファントム** は選択できません。 |
| ペギングされた供給 | バッチ オーダー、製造オーダー、かんばん、移動オーダー、または式明細行に含まれる成分の発注書を作成するため、**ペギングされた供給** を選択します。 関連する注文は、既定の注文設定および成分の生産タイプに基づいて特定され、バッチ オーダーの見積時に作成されます。 バッチ オーダーに必要な成分数量が引当されます。 |
| ベンダー        | 生産プロセスで協力会社を使用し、その協力会社の副生産または発注書を作成する場合は、**ベンダー** を選択します。 協力会社が実行するサービスまたは作業は、式品目またはサービス品目を使用して作成する必要があります。 この品目は、式明細行として親品目に関連付けることができます。 工順には、協力会社の運営ソースに割り当てられる工程を含める必要があります。 この工程は、**工程番号** を使用して式明細行に関連付けられます。 アクションを使用すると、このチェック ボックスは自動的にオンになります。 |

## <a name="formula-versions"></a>フォーミュラ バージョン
新しい式を作成する場合、式明細行品目および固有な特性を追加する前に、式バージョンを作成する必要があります。 どのフォーミュラにも 1 つ以上のバージョンが必要です。 式バージョンの **承認済** ボタンは、バージョン レコードが正常に保存された後にのみ使用できるようになります。 各式のバージョン レコードは、1 つ以上の連産品および副産物に関係づけられ、こられは完成製品の生産時に生産されるかもしれません。 多くの製品は同じ構成要素でも、異なるバッチ サイズで、複数で、または別の歩留りを使用することにより、作成できます。 必要な数だけ式のバージョンを作成できます。

複数の有効な式バージョンを管理するには、有効日の範囲または「開始」数量フィールドを使用します。 複数の有効な式バージョンを持つことができるのは、期間および「開始」数量が重複しない場合だけです。

BOM とは異なり、1 つの BOM は多くの場合複数の BOM バージョンに関連付けられ、各式ごとに 1 つだけ式バージョンが存在します。 1 つの式バージョンだけが、特定の製品の補充分析コードおよび数量に対して有効化できることに注意してください。 ただし、その他の理由により複数の式バージョンが存在し、バッチ オーダーを作成するときそれらを手動で選択することができます。

## <a name="approve-and-activate-formulas-and-formula-versions"></a>式および式バージョンの承認および有効化
式および式バージョンは、計画および生産で使用する前に、事前に承認されている必要があります。 式は、通常使用される前に有効化されます。 ただし、生産中にも承認されている式バージョンを選択できますが、有効化はされていません。

式または式バージョンのセキュリティを確保するには、**編集を防止** および **承認の削除を防止** のパラメーターを **生産管理パラメーター** ページで設定できます。

**編集を防止** を選択し、式を承認する場合は、式明細行のフィールドは削除または編集できません。 ただし、式の承認を削除すると、式明細行を削除および変更できます。 新しい式と新しい式バージョンを作成できます。

**承認の削除を防止** を選択した場合、承認済み式または式バージョンの承認を削除できません。 ただし、新しい式と新しい式バージョンを作成すると、式バージョンの有効化を削除できます。

電子署名機能を使用して、さらに高度な管理を追加できます。 式の承認時に電子署名が必要とされるよう、ユーザー設定されている場合、式が有効になると **署名** ページが表示されます。 変更が確定される前に、ユーザーに電子署名を行う権限が付与されて、証明書が正しく承認される必要があります。 署名が承認されない場合は、承認または承認の削除が拒否され、承認または承認の削除を開始しようとした変更は元の状態に戻されます。

## <a name="use-the-scalable-feature"></a>スケーラブルな機能の使用
スケーラブルな機能は、式のすべての品目コンポーネントが **変動消費** に設定されている場合にのみ使用できます。 品目コンポーネントが **固定消費** または **ステップの消費** に設定されている場合、機能は使用できません。 スケーラブルな機能を使用する場合、式の構成要素を変更すると、選択した他の材料の数量が調整されます。 式サイズも調整されます。 同様に、式サイズを変更すると、すべてのスケーラブルな材料の数量が変更されます。 この機能は、特に式の作成および管理を対象としています。 構成要素の数量がバッチ オーダーで上下に縮小増幅されるかどうかを示していません。

## <a name="use-step-consumption"></a>ステップ消費の使用
ステップ消費では、構成材料の **フォーミュラ明細行** タブに数量を入力する必要がありません。 その代わり、ステップ消費は **シリーズの開始** 値と **数量** 値を持つように構成されます。 バッチ オーダーで選択された数量を満たす一連のレコードごとのステップ消費からの情報。 ステップ消費は、消費係数がバッチ オーダーのサイズに関して直線的でない場合、および特定の数量の閾値が満たされない時に条件のみを高める場合に便利です。 新しい式のこの機能を有効にするには、**消費計算** グループの下で、利用できる構成材料の式設定を **標準** から **ステップ** に変更します。 **式明細行** ページの **設定** タブでこの消費方法を指定します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
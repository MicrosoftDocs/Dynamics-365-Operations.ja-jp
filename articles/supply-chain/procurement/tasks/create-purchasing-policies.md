---
title: 購入ポリシーの作成
description: この記事では、購買の業務プロセスに対応する購入ポリシーを作成する方法を説明します。
author: GalynaFedorova
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a8d42eaf22730f572e2733dec4318e5e4603d74
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2022
ms.locfileid: "9732702"
---
# <a name="create-purchasing-policies"></a>購入ポリシーの作成

[!include [banner](../../includes/banner.md)]

この記事では、購買の業務プロセスに対応する購入ポリシーを作成する方法を説明します。 購買ポリシーを作成する前に、購買ポリシー パラメーターを設定する必要があります。 購入ポリシーの作成、変更、無効は可能ですが、購入ポリシーの削除はできません。 通常、このタスクを実施するのは、購買マネージャーです。 デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。


## <a name="set-up-policy-parameters"></a>ポリシー パラメータの設定
1. ナビゲーション ウィンドウで、**モジュール > 調達 > 設定 > ポリシー > 購買ポリシー** の順に移動します。
2. アクション ウィンドウで、**パラメーター** を選択します。
    - ポリシーの優先順位ルールは、組織内のさまざまなレベルに適用されます。 表示される組織単位は、組織の階層に対応しており、その階層におけるレベルに応じて調達の内部統制についての目的が割り当てられています。 たとえば組織内に法人、コスト センター、地域、部門があるかもしれませんが、これらの一部のみが調達の内部統制の階層についての目的を有しています。 既定として、「会社」タイプの組織が使用できます。  
3. **ポリシー ルール タイプ パラメーター** タブを選択します。
4. ツリーで、**購買ポリシー > 購買請求コントロール ルール** の順に移動します。
    - ポリシー レベルでポリシー解決の優先順位を定義します。 ただし、一部のポリシー タイプについては、個々のポリシー ルール タイプの優先順位を上書きできます。 たとえば、コスト センター、部門、会社の順序で、購買ポリシーの優先順位を定義できます。 カタログ ポリシー ルールでは、優先順位を、部門、コスト センター、会社の順序にされるかもしれません。 カタログ ポリシー ルールについての優先順位を変更できます。 作業者が要求を作成すると、表示されるカタログは、作業者部門と、そしてコスト センター、それから会社と関連付けられるポリシーによって決定されます。  
    - 複数の組織レベルが一覧表示される場合、上/下方向の矢印を使用して [購買要求] の管理ルールの優先順位を設定できます。  
5. ページを閉じます。

## <a name="create-a-new-policy"></a>新しいポリシーの作成
1. **新規** を選択します。
2. **名前** フィールドに値を入力します。
3. **説明** フィールドで、値を入力します。
    - 1 つの購入ポリシーは、1 つの組織階層にのみ適用できます。 たとえば、「地理」 という階層と 「部門」 という階層を設定できますが、それぞれに対して異なる購買ポリシーを設定できます。  
    - ポリシーを適用する組織を選択します。  
4. 矢印を選択して、選択された組織を追加します。
    - このプロセスを繰り返して、さらに組織を追加できます。  

## <a name="add-a-policy-rule"></a>ポリシー ルールの追加
1. **ポリシー ルール タイプ** の一覧で、**請求目的のルール** を選択します。
    - 既定の要求目的を [消費] と入力するように設定し、代わりに [補充] タイプ も選択できるようにルールを作成します。  
2. **ポリシー ルールの作成** を選択します。
3. **手動での上書きを許可** フィールドで、**はい** を選択します。
4. **閉じる** を選択します。
    - 次に、購入ポリシーの他のポリシー ルールを設定できます。 ポリシー ルール タイプでは、1 つの調達ポリシー内で同時に有効なルールを重複させることはできないことに注意してください。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

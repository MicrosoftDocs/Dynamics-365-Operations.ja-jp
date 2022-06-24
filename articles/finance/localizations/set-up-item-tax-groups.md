---
title: 品目の税グループを設定する
description: この記事では、税計算サービスで品目の税グループを設定する方法について説明します。
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 3bc705bc8173ad2bc8ef883e6dc80b0a187314ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846466"
---
# <a name="set-up-item-tax-groups"></a>品目の税グループを設定する

[!include [banner](../includes/banner.md)]

この記事では、税計算サービスで品目の税グループを設定する方法について説明します。 また、品目の税グループ適用ルール マトリックスを設定し、マトリックスで明細行を構成する方法も説明します。

税計算サービスの品目の税グループの概念は、Microsoft Dynamics 365 Finance の品目の消費税グループの概念に似ています。 これは、税コードのグループです。 税計算サービスは、税グループと品目税グループの共通部分を使用して税コードを決定します。

> [!IMPORTANT]
> 税計算サービスにおける品目の税グループの設定は、法人に依存しません。 この設定は、Regulatory Configuration Service (RCS) で一度だけ実行できます。 Finance で税計算サービスを有効にすると、選択した法人に対して品目の税グループが自動的に同期されます。

## <a name="set-up-an-item-tax-group"></a>品目の税グループを設定する 

以下の手順で、品目の税グループを設定します。

1. [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) にサインインします。
2. **ワークスペース** \> **グローバリゼーション機能** \> **税計算** の順に移動します。
3. 設定する機能とバージョンを選択し、**編集** を選択します。
4. **全般** タブで、**構成バージョン** を選択します。
5. **品目の税グループ** タブで、**列の管理** を選択します。 初めて品目税グループを設定する場合は、**列の管理** ダイアログ ボックスのフィールドが自動的に設定されます。
6. 左側の一覧で、**明細行** ノードを展開し、**品目の税グループ** の チェック ボックスを選択します。

    ![列の管理ダイアログ ボックスの明細行ノードで選択された品目の税グループ。](media/select-item-tax-group.png)

7. 右矢印ボタンを選択して、右側の **選択した列** リストに **品目の税グループ** を追加します。

    ![選択した列リストに追加された品目の税グループ。](media/add-item-tax-group.png)

8.  **OK** を選択します。

## <a name="configure-an-item-tax-group"></a>品目の税グループを構成する

品目の税グループを設定すると、税グループの適用ルール マトリックスが作成されます。 マトリックスに明細行を追加して、品目の税グループを構成できます。

1. **品目の税グループ** タブで、**追加** を選択します。
2. **品目の税グループ** フィールドに、品目の税グループの名前を入力します。

    > [!IMPORTANT]
    > 品目の税グループの名前は 10 文字に制限することをお勧めします。 この名前は Finance と同期され、品目の消費税グループの名前の文字数の上限は 10 文字です。

3. **税コード** フィールドで、税グループに含める品目の税コードごとにチェック ボックスを選択します。 1 つの税グループに複数の品目の税コードを含めることができます。

    ![税コード フィールドで選択された複数の税コード。](media/multiple-tax-codes-selection.png)

4. ステップ 1 から 3 を繰り返して、品目の税グループを追加します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

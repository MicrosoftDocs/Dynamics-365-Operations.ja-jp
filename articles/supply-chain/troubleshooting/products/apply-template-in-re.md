---
title: リリースされた製品にテンプレートを適用できない
description: リリースされた製品にテンプレートを適用できない。
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026670"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>リリースされた製品を作成するためにテンプレートを適用できない

KB 番号: 4612097

## <a name="symptoms"></a>現象

**新しいリリースされた製品** ダイアログ ボックスを使用して新しいリリース済製品を作成する場合は、テンプレートを選択できます。 このテンプレートは、新しいリリースされた製品の多くのフィールドに対する既定の設定を提供する必要があります。 ただし、テンプレートを選択した後は、フィールドの一部またはすべてが設定されていないフィールドです。

## <a name="cause"></a>原因

Microsoft Dynamics 365 Supply Chain Management の多くのページでは、それらのページに表示されるレコードの初期設定を確立するテンプレートを作成できます。 これらのテンプレートの 1 つを作成するには、アクション ペインの **オプション** タブで **レコード** 情報を選択します。 ただし、リリースされた製品は他のほとんどのタイプのレコードよりずっと複雑です。 **リリースされた製品** ページで **レコード情報** を選択してテンプレートを作成することもできますが、リリースされた製品を作成するときにそのテンプレートを選択することもできますが、このテンプレートは、新しいリリース済製品の予想されるフィールド値を提供しません。 そのため、リリースされた製品には "レコード情報" テンプレートを使用することはできません。 代わりに、専用の製品テンプレートを作成する必要があります。

## <a name="resolution"></a>解像度

製品テンプレートを作成するには、**オプション** タブの **レコード情報** ボタンではなく、アクション ペインの **製品** タブの **テンプレート** メニューを使用します。

1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. アクション ペインの **製品** タブの **新規** グループで、**テンプレート** を選択し、必要に応じて **個人テンプレートの作成** または **共有テンプレートの作成** を選択します。
